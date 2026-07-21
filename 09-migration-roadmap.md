# Migration Roadmap — 10 Phases

## Phase 1: Inventory & Export (Base44) ✅ Ready
- [x] Export all entity data as JSON/CSV
- [x] Export all frontend source code
- [x] Document all routes from src/App.jsx
- [x] Document all entity schemas (this repo)
- [x] Document all backend functions (this repo)
- [x] Document all agent configs (this repo)
- [x] Export all secrets list
- [x] Export all OAuth connector scopes
- [ ] Screenshot every public page
- [ ] Screenshot every admin page

## Phase 2: Set Up Emergent Project
- [ ] Create account at emergent.sh
- [ ] Create new project — React/Vite scaffold
- [ ] Configure custom domain (gannonwaye.com)
- [ ] Set up environment variables for all secrets
- [ ] Set up Stripe (reuse STRIPE_SECRET_KEY)
- [ ] Set up OpenAI (reuse OPENAI_API_KEY)
- [ ] Set up database matching entity schemas
- [ ] Set up file storage for images/audio
- [ ] Configure OAuth redirect URIs

## Phase 3: Rebuild Public Site
- [ ] Rebuild Home, Music, Store, StoreWorld
- [ ] Rebuild Cart, Checkout, Customer Details
- [ ] Rebuild Lyrics, Gallery, BackThis
- [ ] Rebuild Community, Videos, Contact
- [ ] Rebuild MumTribute, MumsGarden, Memorial
- [ ] Rebuild CurrentSingle, ReleaseDetail
- [ ] Rebuild About, Biography, Press, PressKit
- [ ] Rebuild Coaching pages
- [ ] Rebuild GiftCards, GiftTracker
- [ ] Rebuild Navigation (Navbar, Footer, MobileBottomTabs)
- [ ] Rebuild all other public pages

## Phase 4: Rebuild Admin System
- [ ] Rebuild AdminLayout (sidebar, auth guard, breadcrumbs)
- [ ] Rebuild Dashboard / DailyDashboard
- [ ] Rebuild Orders management
- [ ] Rebuild MerchManagement
- [ ] Rebuild Releases management
- [ ] Rebuild Subscribers, PromoCodes, ShippingRates
- [ ] Rebuild FinancialDashboard
- [ ] Rebuild StripeCommandCentre
- [ ] Rebuild ContentStudio, ContentPipeline
- [ ] Rebuild CoachingPrograms, MeditationLibrary
- [ ] Rebuild MusicProduction, ProducerDirectory
- [ ] Rebuild all other admin pages (200+)

## Phase 5: Rebuild Backend Logic
- [ ] Rebuild Stripe webhook + checkout
- [ ] Rebuild promo code validation
- [ ] Rebuild shipping rate calculation
- [ ] Rebuild order notification chain
- [ ] Rebuild order fulfillment + dedup
- [ ] Rebuild email sending (welcome, receipts, reminders)
- [ ] Rebuild AI content generation
- [ ] Rebuild social posting (Instagram, TikTok)
- [ ] Rebuild Metricool integration
- [ ] Rebuild site health checks
- [ ] Rebuild all other functions (130+)

## Phase 6: Rebuild Agent System
- [ ] Rebuild orchestrator
- [ ] Rebuild music_orchestrator
- [ ] Rebuild revenue_orchestrator
- [ ] Rebuild fan_engagement_agent
- [ ] Rebuild literature_researcher
- [ ] Rebuild academic_writing_coach
- [ ] Rebuild all 31 agents
- [ ] Rebuild agent memory system
- [ ] Rebuild agent approval queue

## Phase 7: Rebuild Automations
- [ ] Rebuild scheduled automations
- [ ] Rebuild entity-triggered automations
- [ ] Rebuild connector webhook automations
- [ ] Rebuild Stripe webhook automation
- [ ] Rebuild TikTok webhook automation

## Phase 8: Data Migration
- [ ] Migrate MerchProduct records
- [ ] Migrate MerchOrder records (historical)
- [ ] Migrate StoreCustomer records
- [ ] Migrate EmailSubscriber records
- [ ] Migrate Release + Lyric records
- [ ] Migrate PromoCode, GiftCard records
- [ ] Migrate SupportContribution records
- [ ] Migrate community records (comments, posts)
- [ ] Migrate settings (BusinessProfileSettings, SiteSettings)
- [ ] Migrate all media URLs (re-upload if storage changes)
- [ ] Verify data integrity

## Phase 9: Parity Testing
- [ ] All public pages load correctly
- [ ] Store: products, pricing, cart, checkout
- [ ] Stripe webhooks fire and create orders
- [ ] Order deduplication works
- [ ] Promo code rules enforced
- [ ] Email notifications send
- [ ] Admin dashboard protected and functional
- [ ] Agent system responds
- [ ] Mobile responsive
- [ ] Full test order completed
- [ ] Community features work
- [ ] Gallery displays images
- [ ] Meditation audio plays

## Phase 10: Domain Cutover
- [ ] Freeze Base44 — no more changes
- [ ] Final data export from Base44
- [ ] Final data import to Emergent
- [ ] Deploy Emergent to production
- [ ] Run smoke tests
- [ ] Switch DNS: gannonwaye.com → Emergent
- [ ] Update Stripe webhook URL
- [ ] Update all OAuth redirect URIs
- [ ] Monitor checkout for 48 hours
- [ ] Retire Base44 after confirmed stable
