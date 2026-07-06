# Example: E-commerce Checkout Psychology Review

> Demonstrates applying psychology principles to reduce cart abandonment.

## Prompt
"Our checkout flow has a 68% cart abandonment rate. Review through a psychology lens."

## Review Output

### Where Users Are Dropping Off (Psychology Diagnosis)

**Cart → Shipping Info (32% drop)**
- **Cognitive Load violation:** Requiring account creation before checkout forces a decision the user didn't come to make
- **Fix:** Guest checkout option. Ask for account creation AFTER purchase (Commitment/Consistency — they've already bought, so saving info for next time is a small ask)

**Shipping Info → Payment (22% drop)**
- **Loss Aversion triggered:** Shipping costs appearing for the first time at this step triggers "hidden cost" reaction
- **Fix:** Show shipping estimate earlier (product page or cart). Transparency reduces the pain of payment

**Payment → Confirmation (14% drop)**
- **Trust gap:** Users hesitate at the payment step when they don't see enough security signals
- **Fix:** Add trust badges (SSL, money-back guarantee, review count) NEXT TO the payment button, not in the footer

### Principles to Apply

| Principle | Implementation | Expected Impact |
|-----------|---------------|-----------------|
| Cognitive Load | Guest checkout, minimal form fields | Reduces cart→shipping drop |
| Transparency | Show total cost (including shipping) on product page | Reduces shipping→payment drop |
| Authority + Social Proof | Trust badges adjacent to payment button | Reduces payment→confirmation drop |
| Progress Indicator | "Step 2 of 3" bar at top | Zeigarnik Effect pulls users through |
| Default Effect | Pre-select standard shipping, pre-check "save info" | Reduces decision points |
| Peak-End Rule | Confirmation page with order summary + "you saved $X" | Ends on positive note, increases return rate |

### What NOT to Do

- Don't add a "related products" carousel at checkout — that's misdirection away from conversion
- Don't require phone number unless needed for delivery — every unnecessary field increases abandonment
- Don't show a countdown timer on the cart — fake urgency erodes trust
