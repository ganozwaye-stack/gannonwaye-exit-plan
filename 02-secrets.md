# Secrets & Environment Variables

> 13 secrets to configure on the new platform

## Critical Secrets (set first)

### `STRIPE_SECRET_KEY`
- **Description:** Stripe payment processing — server-side
- **Action:** Reuse on Emergent

### `STRIPE_PUBLISHABLE_KEY`
- **Description:** Stripe client-side key
- **Action:** Reuse on Emergent

### `STRIPE_WEBHOOK_SECRET`
- **Description:** Stripe webhook signature verification
- **Action:** Re-register webhook URL, get new secret

### `OPENAI_API_KEY`
- **Description:** OpenAI for AI agents, content generation
- **Action:** Reuse on Emergent

## Optional Secrets

### `GITHUB_TOKEN`
- **Description:** GitHub API for code management
- **Action:** Reuse on Emergent

### `CURSOR_API_KEY`
- **Description:** Cursor IDE integration
- **Action:** Reuse if needed

### `HEYGEN_API_KEY`
- **Description:** HeyGen avatar video generation
- **Action:** Reuse on Emergent

### `METRICOOL_BLOG_ID`
- **Description:** Metricool social scheduling blog ID
- **Action:** Reuse on Emergent

### `METRICOOL_USER_ID`
- **Description:** Metricool user ID
- **Action:** Reuse on Emergent

### `METRICOOL_API_TOKEN`
- **Description:** Metricool API access token
- **Action:** Reuse on Emergent

### `TIKTOK_CLIENT_KEY`
- **Description:** TikTok OAuth client key
- **Action:** Re-register redirect URI

### `TIKTOK_CLIENT_SECRET`
- **Description:** TikTok OAuth secret
- **Action:** Reuse, update redirect URIs

### `GOOGLE_SHEET_ID`
- **Description:** Google Sheets sync sheet ID
- **Action:** Reuse on Emergent

## Setup Instructions

1. On Emergent, go to Project Settings → Environment Variables
2. Add each secret above with its value (values are NOT exported — enter manually)
3. For Stripe webhook secret: register new webhook URL on Stripe Dashboard after deploy, then set the new signing secret
4. For TikTok: update redirect URIs to the new platform's callback URL
