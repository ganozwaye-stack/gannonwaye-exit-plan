# System Architecture

## Overview

The Gannon Waye platform is a full-stack music artist website with:
- **Frontend:** React + Vite + Tailwind CSS + shadcn/ui
- **Backend:** Base44 BaaS (entities, functions, automations, agents)
- **Payments:** Stripe (Checkout Sessions, Payment Intents, Webhooks)
- **AI:** OpenAI (content generation, agents), HeyGen (avatar videos)
- **Social:** Instagram, TikTok, Metricool (scheduling)
- **Integrations:** Google (Calendar, Drive, Sheets, Gmail), Slack

## Key Flows

### Store Checkout Flow
1. Customer browses `/store` → adds to cart
2. Cart → `/store/customer-details` → `/store/checkout`
3. Frontend calls `createCheckoutSession` backend function
4. Stripe Checkout Session created with line items
5. Customer pays on Stripe → redirects to `/checkout-success` or `/checkout-cancel`
6. Stripe webhook fires → `stripeWebhook` function creates MerchOrder
7. Order dedup via `orderLockingMiddleware` / `OrderLock` entity
8. Notifications: `notifyAdmin`, `sendOrderReceipt`, `onNewOrderSlack`
9. Order synced to Google Sheets via `syncOrderToSheets`

### Promo Code Flow
1. Customer enters code at checkout
2. Frontend calls `validatePromoCode` backend function
3. Validates: active, not expired, usage limits, category exclusions
4. Returns discount amount → frontend recalculates totals
5. `applyCheckoutDiscountGuard` enforces rules server-side
6. `recordPromoUsage` increments usage count

### Agent System Flow
1. Agent receives task (from schedule, entity trigger, or chat)
2. Agent uses tools (entity CRUD, backend functions, connectors)
3. Agent creates `AgentActionProposal` for approval-gated actions
4. `ApprovalQueue` → admin reviews → `proofApprovalChain`
5. `publishApprovedProposal` executes approved action
6. `agentIntelligenceLoop` learns from outcomes
7. `agentSelfImprovement` updates agent instructions

### Release Pipeline Flow
1. Release created in admin (`/admin/releases`)
2. Status tracked: idea → writing → recording → mixing → mastering → ready → released
3. `releaseCalendarSync` adds to Google Calendar
4. `notifySubscribersNewRelease` emails subscribers
5. `generateReleaseSprint` creates action plan
6. `generatePresaveLinks` creates pre-save links

### Memorial Flow
1. Fan visits `/remember-mum` or `/mums-garden`
2. Can submit memories via `onMemorySubmission`
3. `soniaChat` provides AI chat with mum's personality
4. Memorial visual director agent manages visual content

## Data Relationships

```
User (auth) ─┬─ MerchOrder ─── MerchProduct
             ├─ EmailSubscriber
             ├─ SupportContribution
             ├─ StoreCustomer
             └─ FanPost ─── FanComment ─── CommunityReply

Release ─┬─ Lyric
         ├─ GalleryImage (artwork)
         └─ ContentPipelineItem

CoachingOffer ─┬─ CoachingLead ─── CoachingIntake ─── CoachingClient
               ├─ CoachingSession
               └─ CoachingWorkbook

MerchProduct ─┬─ MerchFeedback
              ├─ ProductReview
              ├─ MerchInterest
              └─ InventoryBatch ─── PurchaseOrder
```

## Security Model

- **Public read:** entities with `is_published: true` or `is_public: true`
- **Admin only:** create/update/delete on most entities (role = 'admin')
- **User-scoped:** MerchOrder, GiftCard, FanReminder (user.email match)
- **No auth needed:** MerchOrder create (checkout), EmailSubscriber create, FanReminder create
- **Admin route guard:** `/admin/*` routes check user.role === 'admin'
