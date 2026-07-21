# Data Migration Guide

## Export from Base44

### Method 1: Dashboard Export
1. Go to Base44 dashboard → Entities
2. For each entity, click Export (CSV or JSON)
3. Download all files

### Method 2: Bulk Export (exec_tool)
Use the Base44 exec tool to bulk export all entity data:

```javascript
// Run this in Base44 exec_tool for each entity
const data = await base44.asServiceRole.entities.MerchOrder.list('-created_date', 10000);
return data;
```

### Critical Entities to Export First

1. **MerchProduct** — all products with pricing
2. **MerchOrder** — all historical orders
3. **StoreCustomer** — customer profiles
4. **EmailSubscriber** — newsletter list
5. **Release** — songs/albums with lyrics and links
6. **Lyric** — lyrics with publishing status
7. **PromoCode** — active promo codes
8. **GiftCard** — gift card codes and balances
9. **SupportContribution** — donation history
10. **BusinessProfileSettings** — business config
11. **SiteSettings** — site feature toggles
12. **GalleryImage** — gallery photos (URLs only — re-upload images)
13. **CoachingOffer** — coaching programs
14. **Meditation** — meditation audio (URLs only — re-upload audio)
15. **ShippingRateRule** — shipping rules

## Import to Emergent

1. Format exported data to match Emergent's database schema
2. Use Emergent's bulk import or API to insert records
3. For media URLs: if storage platform changes, re-upload all images/audio and update URLs
4. Verify record counts match between Base44 and Emergent
5. Run data integrity checks (spot check orders, products, subscribers)

## Media Files

Images and audio are stored as URLs (Base44 file storage). On Emergent:
1. Download all images from Base44 file URLs
2. Upload to Emergent's file storage
3. Update all `image_url`, `artwork_url`, `audio_url` fields with new URLs

## Stripe Data

Stripe data (customers, charges, subscriptions) stays in Stripe — no migration needed.
Only the webhook endpoint URL needs updating after DNS cutover.
