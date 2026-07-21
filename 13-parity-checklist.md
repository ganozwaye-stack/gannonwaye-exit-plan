# Parity Testing Checklist

> Complete this checklist before switching DNS to the new platform

## Public Pages
- [ ] Home page loads with hero, music, CTAs
- [ ] Music page shows discography
- [ ] Store shows products with correct pricing
- [ ] Product detail pages work
- [ ] Cart adds/removes items
- [ ] Customer details form works
- [ ] Checkout completes via Stripe
- [ ] Checkout success page shows order confirmation
- [ ] Lyrics page shows published lyrics
- [ ] Gallery displays images
- [ ] Contact form sends email
- [ ] Press kit shows photos, bio, links
- [ ] About/Biography pages render
- [ ] Mum Tribute / Memorial pages render
- [ ] Community page shows fan wall
- [ ] Videos page embeds videos
- [ ] FAQ page renders
- [ ] Privacy Policy / Terms render
- [ ] Mobile responsive on all pages

## Store & Checkout
- [ ] Products display with correct pricing
- [ ] Cart calculates totals correctly
- [ ] Promo codes validate and apply discount
- [ ] Shipping rates calculate correctly
- [ ] Stripe checkout session creates successfully
- [ ] Payment completes
- [ ] Order created in database after payment
- [ ] Order deduplication works (no duplicate orders)
- [ ] Order receipt email sent to customer
- [ ] Admin notification sent
- [ ] Order synced to Google Sheets
- [ ] Gift card purchase flow works
- [ ] Support/donation flow works

## Admin System
- [ ] Admin login protected (non-admins blocked)
- [ ] Dashboard loads with data
- [ ] Orders list shows all orders
- [ ] Merch management CRUD works
- [ ] Releases management CRUD works
- [ ] Promo codes management works
- [ ] Shipping rates management works
- [ ] Content studio works
- [ ] Lyrics archive works
- [ ] Coaching programs management works
- [ ] File uploads work (images, audio)

## Automations
- [ ] Daily revenue email sends at 7am
- [ ] Fan reminders send on schedule
- [ ] Birthday discounts send
- [ ] New order triggers notifications
- [ ] New subscriber triggers welcome email
- [ ] Stripe webhook creates orders
- [ ] Google Calendar sync works
- [ ] Social posting works (Instagram, TikTok)

## Agents (if applicable)
- [ ] Agent system responds to chat
- [ ] Agent approval queue works
- [ ] Agent creates proposals
- [ ] Agent memory persists

## Performance
- [ ] Pages load in under 3 seconds
- [ ] No console errors
- [ ] No secrets exposed in frontend
- [ ] SSL certificate valid
- [ ] Custom domain configured
