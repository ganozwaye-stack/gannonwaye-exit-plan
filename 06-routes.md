# Route Map

> Complete list of all routes in the application

## Public Routes (59)

| Path | Page | Description |
|------|------|-------------|
| `/` | Home | Landing page — hero, story, music, CTAs |
| `/music` | Music | Discography, streaming links |
| `/store` | Store World | Immersive store entrance |
| `/store/all` | Store | Full product grid |
| `/store/cart` | Cart | Shopping cart |
| `/store/customer-details` | Customer Details | Checkout customer info |
| `/store/cart-details` | Cart Details | Cart summary |
| `/store/checkout` | Checkout | Stripe checkout |
| `/store/product/:slug` | Product Detail | Individual product page |
| `/videos` | Videos | Video gallery |
| `/lyrics` | Lyrics | Tabbed lyrics archive |
| `/release/:id` | Release Detail | Individual release page |
| `/gallery` | Gallery | Photo gallery |
| `/press-kit` | Press Kit | Media kit with photos, bio, links |
| `/press` | Press | Press page |
| `/about` | About | About Gannon |
| `/biography` | Biography | Full biography |
| `/contact` | Contact | Contact form |
| `/back-this` | Support | Fan support/donation page |
| `/community` | Community | Fan wall, comments |
| `/fan-leaderboard` | Fan Leaderboard | Top supporters |
| `/gift-cards` | Gift Cards | Purchase gift cards |
| `/mixing-services` | Mixing Services | Mixing service page |
| `/discover` | Music Recommender | Song recommender |
| `/fan-reminders` | Fan Reminders | Set reminder emails |
| `/current-single` | Current Single | Featured single page |
| `/upcoming-music` | Upcoming Music | Upcoming releases |
| `/founding-supporter` | Founding Supporter | Founding supporter page |
| `/merch-feedback` | Merch Feedback | Product feedback form |
| `/order-status` | Order Status | Check order status |
| `/orders` | Order History | Customer order history |
| `/email-preferences` | Email Preferences | Manage email prefs |
| `/remember-mum` | Remember Mum | Memorial page |
| `/mums-garden` | Mum's Garden | Garden memorial |
| `/memorial` | Memorial | Memorial page |
| `/live` | Live | Livestream page |
| `/presave` | Pre-Save | Pre-save campaign |
| `/checkout-success` | Checkout Success | Post-purchase success |
| `/checkout-cancel` | Checkout Cancel | Post-purchase cancel |
| `/faq` | FAQ | Frequently asked questions |
| `/privacy-policy` | Privacy Policy | Privacy policy |
| `/terms-of-service` | Terms of Service | Terms of service |
| `/this-is-my-life` | This Is My Life | Story page |
| `/summary` | Summary | Site summary |
| `/member-tiers` | Member Tiers | Membership tiers |
| `/impact` | Impact | Impact page |
| `/portrait-gallery` | Portrait Gallery | Portrait photos |
| `/tour` | Tour | Tour dates |
| `/bookings` | Bookings | Booking enquiry |
| `/systems-manager` | Systems Manager Offer | Platform as a service offer |
| `/systems/cinematic-websites` | Cinematic Websites | Case study |
| `/systems/case-studies/gannon-waye-music-os` | Case Study: Music OS | Case study |
| `/systems/case-studies/ganozmix-direct` | Case Study: GanozMix | Case study |
| `/lyric-library` | Lyric Library | Lyric collection |
| `/support/domestic-violence` | DV Support | Domestic violence resources |
| `/embed-timer` | Embed Timer | Embeddable countdown timer |
| `/tiktok-platform-review` | TikTok Review | TikTok platform review |
| `/tiktok-callback` | TikTok Callback | TikTok OAuth callback |
| `/gift-checklist` | Gift Checklist | Gift checklist |

## Admin Routes (200+)

All admin routes are under `/admin/*` and require admin authentication.

### Key Admin Routes

| Path | Description |
|------|-------------|
| `/admin/dashboard` | Daily dashboard |
| `/admin/releases` | Release management |
| `/admin/merch` | Merch product management |
| `/admin/orders` | Order management |
| `/admin/subscribers` | Email subscriber management |
| `/admin/fans` | Fan management |
| `/admin/settings` | Site settings |
| `/admin/financials` | Financial dashboard |
| `/admin/promo-codes` | Promo code management |
| `/admin/shipping-rates` | Shipping rate rules |
| `/admin/content-studio` | Content studio |
| `/admin/lyrics-archive` | Lyrics management |
| `/admin/coaching-hub` | Coaching hub |
| `/admin/production-tracker` | Production tracker |
| `/admin/press-kit` | Press kit admin |
| `/admin/gallery` | Gallery management |
| `/admin/merch-visual-lab` | Merch visual lab + AI mockup generator |
| `/admin/communications-hub` | Communications hub |
| `/admin/stripe-command-centre` | Stripe command centre |
| `/admin/approval-queue` | Agent approval queue |

## Router File

The router is in `src/App.jsx`. It contains:
- `<AuthProvider>` wrapper
- `<QueryClientProvider>` wrapper
- `<BrowserRouter>` wrapper
- `<Routes>` with all `<Route>` elements
- Public routes wrapped in `<PublicLayout />` (Outlet)
- Admin routes wrapped in `<AdminLayout />` (Outlet)
- Auth guard checks admin role for `/admin/*` routes
