# Emergent Setup Guide

## Step 1: Create Project

1. Go to [emergent.sh](https://emergent.sh)
2. Create a new project
3. Choose React + Vite scaffold
4. Set project name: `gannonwaye`

## Step 2: Environment Variables

Set these in the Emergent project settings:

```env
STRIPE_SECRET_KEY=sk_live_...
STRIPE_PUBLISHABLE_KEY=pk_live_...
OPENAI_API_KEY=sk-...
GITHUB_TOKEN=ghp_...
HEYGEN_API_KEY=...
METRICOOL_BLOG_ID=...
METRICOOL_USER_ID=...
METRICOOL_API_TOKEN=...
TIKTOK_CLIENT_KEY=...
TIKTOK_CLIENT_SECRET=...
GOOGLE_SHEET_ID=...
```

## Step 3: Database

Create tables matching the schemas in `01-entities/all-schemas.json`.

Key tables (critical):
- `releases` — songs, albums
- `lyrics` — lyrics with publishing status
- `merch_products` — products with pricing/cost
- `merch_orders` — orders with Stripe IDs
- `store_customers` — customer profiles
- `promo_codes` — discount codes
- `gift_cards` — gift card codes
- `support_contributions` — fan donations
- `email_subscribers` — newsletter subscribers

Add Row Level Security (RLS) matching the Base44 RLS rules in each schema:
- Public read: where `is_published = true`
- Admin create/update/delete: where `user.role = 'admin'`
- User-scoped read: where `customer_email = user.email`

## Step 4: File Storage

Set up file storage for:
- Product images
- Release artwork
- Gallery photos
- Audio files (meditations, music previews)
- Fan-uploaded media

## Step 5: Stripe

1. Reuse STRIPE_SECRET_KEY and STRIPE_PUBLISHABLE_KEY
2. Register new webhook URL: `https://gannonwaye.com/api/stripe-webhook`
3. Events to listen for: `checkout.session.completed`, `payment_intent.succeeded`, `payment_intent.payment_failed`
4. Get new webhook signing secret → set as STRIPE_WEBHOOK_SECRET

## Step 6: OAuth Connectors

For each connector in `03-connectors.md`:
1. Register OAuth app (if not already)
2. Set redirect URI to Emergent callback URL
3. Authorize the connection

## Step 7: Deploy

1. Push all source code to the Emergent project
2. Configure custom domain
3. Deploy to production
4. Test all flows from `13-parity-checklist.md`

## Step 8: DNS Cutover

1. Update DNS A/CNAME records to point to Emergent
2. Update Stripe webhook URL
3. Update all OAuth redirect URIs
4. Monitor for 48 hours
