# Cart flow + AOV research — $30 MCC tester, cold Meta traffic (2026-06-24)

**Question:** post-add-to-cart flow that maximizes BOTH conversion + AOV for a $30 single-product clean-beauty offer on cold paid social. Slide cart drawer vs full cart page vs direct-to-checkout; where to place the upsell.

## Recommendation
Keep it lean — **no heavy full cart-PAGE step** (it's the option most likely to hurt conversion). Put **ONE optional, clearly-priced add-on at the cart stage, shown AFTER the tester is added** (slide drawer / lean cart). It can't lower the tester conversion (commitment already made), can't confuse the $30 offer (cart shows what they're buying), and is pre-checkout so **every payment method sees it** — including the express wallets that the post-purchase upsell misses. Do NOT rely on post-purchase as the main AOV lever.

## Verified findings (HIGH confidence — Baymard + Shopify docs + 6 upsell vendors)
1. **A separate cart PAGE adds friction = abandonment risk.** Global cart abandonment ~70%; ~18% of US shoppers abandon specifically because checkout is too long/complicated; avg checkout bloated (23.48 form elements vs ideal 12–14). Fewer steps = less drop-off.
2. **Shopify post-purchase upsells are SKIPPED for express wallets + installments** — Apple Pay, Google Pay, Amazon Pay, Klarna, Affirm, Afterpay, Shop Pay 4-installment, gift-card-only. Only full-payment Shop Pay, PayPal Express, and direct credit card qualify (payment must be vaulted; wallet redirects prevent it). THE central caveat for cold mobile Meta traffic.
3. **Express checkout buttons can appear on the PDP** and let shoppers skip the cart (and its upsells) entirely.
4. Baymard's "~35% conversion lift from better checkout UX" is a large-site theoretical ceiling, not a single-product DTC expectation.

## Honest caveat — AOV magnitude is UNVERIFIED
Every specific AOV-lift % and upsell-acceptance-rate stat in the source pool FAILED adversarial verification (all refuted 0-3): the "+10–30% AOV," "4–8% FBT acceptance," "17% in-cart lift across 312 Shopify Plus brands," "post-purchase converts 5–10× higher," the "cart-drawer-wins 3.45% test," "+10–20% post-purchase AOV," and "PayPal-in-drawer +37%." These were unsourced CRO/app blog claims. So the recommendation rests on friction/abandonment data + documented platform mechanics — NOT on quantified lift numbers. Don't cite specific %; learn magnitude from live data.

## Open question that refines the plan
What share of this store's checkouts are express wallets (Apple/Google Pay) vs card/Shop Pay? High express share → the cart-stage add-on is essential (post-purchase can't reach them). Pull from Shopify before finalizing.

## Practical note for THIS LP→store flow
LP buy buttons currently navigate to the Shopify **cart page** (`/cart/...`). A true slide-out drawer is an on-site overlay (needs a Shopify cart-upsell app like Rebuy/AfterSell/iCart or theme dev) and mainly applies to on-site browsing; external LP links land on the cart page. So the cart-stage add-on for LP traffic = a clean cart-page upsell OR a pre-checkout add-on on the LP buy box that rides into checkout. Either way: pre-checkout, optional, one add-on, after the tester decision.

## DECISION (2026-06-24): Option 2
Main CTA stays direct-to-checkout. Add ONE optional one-click add-on block under the buy box (optionally mirror once at the bottom CTA). Default OFF, minimal info (image + 1 benefit line + price + toggle), framed as "complete your order" — accept-or-ignore, not a decision. Add-on rides into the order via multi-item cart permalink (`/cart/{tester}:{q},{addon}:1`). Pair with a thank-you/order-status page upsell (reaches express-pay buyers the native post-purchase misses). Avoid Option 3 (slide cart = forced step, hurts mobile).

### Add-on product candidates (verified variant IDs + prices, 2026-06-24)
- **Citrus Toning Mist (120ml) — $19.95 — variant 48241799725313** ← recommended (cheap, universal, complements makeup, easiest yes)
- Matcha Melt Makeup Remover Balm-to-Milk (2oz) — $30.00 — variant 48241840226561 (great theme match, but doubles order / bigger ask)
- MYCO Silk Eye Cream (1oz) — $37.95 — variant 49222335627521 (LTV-bridge; better for thank-you page / email)
- AVOID as add-on: single colour creams ($24.95 — value-confusing vs 3-for-$30, forces a shade decision); Premium Ozonated Age-Defying Cream ($69.95 — too pricey/specialty).
- Tester (core) variant: 46591897567489 ($30). See [[project_mcc_tester_variant_id]].

_Full cited report: deep-research run wf_9f6b6033-9cd._
