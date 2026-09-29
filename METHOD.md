# Method: Shopify app costs (StoreCartel)

Checked 2026-09-28. 18 apps, 57 plans, six categories: upsell (Zipify OCU, ReConvert, AfterSell), reviews (Judge.me, Loox, Yotpo), email/SMS (Klaviyo, Omnisend, Privy), dropshipping (AutoDS, DSers, Zendrop), print on demand (Printful, Printify, Gelato), page builders (GemPages, PageFly, Shogun).

## Sources
Every price, plan limit, rating and review count comes from the app's own Shopify App Store listing (`https://apps.shopify.com/<slug>`), fetched on the checked date. The pricing block on a listing is authored by the vendor and is what Shopify bills. Rating and review count are the values shown on that page on that date. Currency is USD as billed on the listing. `annualUsdPerMonth` is the listed yearly price divided by 12 (our arithmetic). Vendor websites were not used, so vendor-site-only items (order-tiered ladders, add-on fees) are gaps, not guesses.

## Derived: monthly stack cost at 100 / 500 / 2,000 orders (stacks.json)
Rules: cheapest listed plan whose stated limit covers the volume; monthly billing; free trials ignored; extras only where the listing states a formula.
- Dropshipping starter: DSers Advanced $19.90 + ReConvert Growth $9.99 (Free covers only 50 orders; Growth covers 2,000) + Judge.me Free + GemPages Free = $29.89 at all three volumes.
- Upsell-heavy brand: AfterSell Post-Purchase $34.99 + Loox + PageFly Builder $24. Loox is free to 500 orders; at 2,000 the Convert formula ($49.99 + $50 per extra 300 orders = $349.99) exceeds Unlimited $299.99, so Unlimited is used. Totals $58.99 / $58.99 / $358.98.
- Print-on-demand store: Printify Premium $39 + Judge.me Awesome $15 + ReConvert Growth $9.99 + PageFly Free = $63.99 at all volumes.
Not included: Printful/Printify/Gelato product and shipping costs, payment processing, Shopify's own plan, email/SMS (priced by contacts, not orders), and Zipify (priced by upsell revenue). Order-independent totals reflect these plans' pricing, not an error.

## Re-check cadence
Every 90 days, or when a listed vendor changes pricing. Update `checked` per record only when re-fetched.
