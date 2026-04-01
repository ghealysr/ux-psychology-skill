# UX Psychology Skill

> Advisory layer for web design decisions. Surfaces relevant behavioral psychology principles during page and component design. This is a **weighted input** — it informs decisions, it does not override aesthetic judgment, brand identity, or creative direction.

## When to Use

Invoke after building or designing pages, components, or flows. The skill works best as a **review layer** — build first, then run the psychology lens to find what you're missing:

- Landing pages, pricing pages, onboarding flows
- Subscription/conversion funnels
- Dashboard layouts and data presentation
- Navigation and information architecture
- E-commerce product pages and checkout flows
- Any page where you want users to take a specific action

## Decision Process

When activated, follow this order:

1. **Identify the page type** — landing, pricing, onboarding, dashboard, checkout, etc.
2. **Pull the 3-5 most relevant principles** from the page-type prescriptions below
3. **For each principle, state:** what it is → how to apply it to THIS specific page → what the anti-pattern looks like
4. **Weight against constraints** — brand identity, accessibility, and technical requirements always take priority
5. **Recommend specific, implementable changes** — not abstract advice. Show what to change in the markup, layout, or copy. If you can point to a line of code, do it.

## How to Weight

Psychology principles are **one input among many**. The weighting hierarchy:

1. **Brand identity and creative vision** (highest — the site must look and feel right)
2. **Accessibility and usability** (non-negotiable — WCAG compliance, touch targets, contrast)
3. **Technical quality** (performance, SEO, responsive design)
4. **Psychology principles** (this skill — subtle influence, not heavy-handed manipulation)

Never sacrifice aesthetics or user trust for a psychology trick. If a principle conflicts with good design, good design wins.

## What This Skill Is NOT

- NOT a dark patterns handbook — every principle here is ethical application only
- NOT a complete design system — it augments existing design skills
- NOT a replacement for user research — real user data always beats theory
- NOT a rigid checklist — use the principles that fit, ignore the ones that don't

---

## Page-Type Prescriptions (Inline)

The top principles per page type, self-contained for quick reference. See `knowledge/page-prescriptions.md` for expanded guidance and common mistakes.

### Homepage / Landing Page
| Principle | Application |
|-----------|------------|
| **First Impressions** | Hero communicates value in under 3 seconds. Formed in 50ms — no second chances. |
| **Anchoring** | Lead with your strongest metric or claim. First number seen sets the reference. |
| **Social Proof** | Real numbers visible early (users, results, track record). Vague claims don't convert. |
| **Information Scent** | Clear navigation — user knows exactly where to go next. |
| **Aesthetic-Usability** | Visual polish earns trust before content does. Beautiful feels easier to use. |

### Pricing / Subscription
| Principle | Application |
|-----------|------------|
| **Anchoring** | Show premium tier first or most visually prominent. Everything else feels like a deal. |
| **Loss Aversion** | Frame around what free users MISS, not just what paid users get. Losing hurts 2x more. |
| **Default Effect** | Pre-select the recommended tier. Most users never change defaults. |
| **Commitment/Consistency** | Users who already used free features are primed to subscribe — each step leads to the next. |

### Onboarding / Sign-Up
| Principle | Application |
|-----------|------------|
| **Progressive Commitment** | Small free action first, account second, payment last. |
| **Cognitive Load** | One question per screen beats a long form. Remove everything non-essential. |
| **Zeigarnik Effect** | Show progress (step 2 of 4). Incomplete tasks nag — users come back to finish. |
| **Reciprocity** | Give value before asking for info. Free tool access, preview, or sample result. |

### Dashboard / Data Display
| Principle | Application |
|-----------|------------|
| **Chunking** | Group data by category or priority — not one giant list. |
| **Spatial Memory** | Consistent layout so returning users find things instantly. Don't move things. |
| **Satisficing** | Highlight the single most important insight. Users pick the first acceptable option. |
| **Recognition Over Recall** | Show full context (labels, timestamps, icons) — don't make users remember. |

### Checkout / Payment
| Principle | Application |
|-----------|------------|
| **Cognitive Load** | Guest checkout option. Minimal form fields. One decision at a time. |
| **Transparency** | Show ALL costs before the payment step. Surprise fees are the #1 abandonment cause. |
| **Loss Aversion** | Trust badges and guarantees NEXT TO the payment button, not in the footer. |
| **Default Effect** | Pre-select standard shipping. Pre-check "save info." Reduce decisions. |

### About / Trust Page
| Principle | Application |
|-----------|------------|
| **Authority** | Methodology, data sources, team expertise — prove you know what you're doing. |
| **Hierarchy of Trust** | This page serves users at level 2-3 (interest → confidence). Don't ask for the sale here. |
| **Transparency** | Honest about limitations, not just strengths. Vulnerability builds trust. |

---

## Code-Level Implementation Examples

### Anchoring (Pricing Page)

**Before** — all tiers equal, no anchor:
```html
<div class="plans">
  <div class="plan">Basic — $19/mo</div>
  <div class="plan">Pro — $49/mo</div>
  <div class="plan">Enterprise — $99/mo</div>
</div>
```

**After** — Pro anchored as the visual default:
```html
<div class="plans">
  <div class="plan">Basic — $19/mo</div>
  <div class="plan featured">        <!-- visually prominent, pre-selected -->
    <span class="badge">Most Popular</span>
    Pro — $49/mo
  </div>
  <div class="plan">Enterprise — $99/mo</div>
</div>
```
**Why:** The featured tier becomes the anchor. Basic feels like a bargain by comparison. Enterprise exists to make Pro look reasonable. The "Most Popular" badge adds social proof.

### Loss Aversion (Subscription CTA)

**Before** — gain-framed:
```html
<button>Get Premium Access</button>
<p>Unlock all features and premium content.</p>
```

**After** — loss-framed:
```html
<button>Keep My Premium Access</button>
<p>Without Premium, you'll lose access to daily insights,
   saved dashboards, and priority support.</p>
```
**Why:** "You'll lose access" triggers loss aversion (~2x stronger than equivalent gains). The CTA uses "Keep" — framing it as protecting something they already have.

### Zeigarnik Effect (Onboarding Progress)

**Before** — no progress indication:
```jsx
<form>
  <h2>Tell us about yourself</h2>
  {/* 8 fields on one page */}
</form>
```

**After** — stepped with visible progress:
```jsx
<div className="progress-bar">
  <div className="step completed">Profile</div>
  <div className="step active">Preferences</div>   {/* current */}
  <div className="step">Review</div>
</div>
<form>
  <h2>Step 2 of 3 — Your Preferences</h2>
  {/* 2-3 fields only */}
</form>
```
**Why:** Incomplete progress bars create psychological tension. Users return to finish what they started. Breaking 8 fields into 3 steps of 2-3 fields reduces cognitive load AND creates the pull to complete.

### Cognitive Load (Checkout)

**Before** — forced account creation:
```html
<h2>Create Account to Continue</h2>
<input placeholder="Email" />
<input placeholder="Password" />
<input placeholder="Confirm Password" />
<button>Create Account & Checkout</button>
```

**After** — guest checkout with deferred account creation:
```html
<h2>Checkout</h2>
<input placeholder="Email (for receipt)" />
<button>Pay Now</button>
<p class="subtle">Want to save your info for next time?
   <a href="/create-account">Create an account</a> after checkout.</p>
```
**Why:** Every extra field is a decision point that causes abandonment. Get the sale first. Account creation is a small ask AFTER they've already committed (Commitment/Consistency principle).

---

## Principle Categories (11)

| Category | Count | Core Insight |
|----------|-------|--------------|
| Attention | 4 | Users see less than you think |
| Gestalt | 8 | Visual grouping drives comprehension |
| Memory | 10 | Recognition beats recall; chunk everything |
| Sensemaking | 3 | Mental models shape expectations |
| Decision Making | 5 | Fewer choices, clearer outcomes |
| Motor/Interaction | 3 | Big targets, fast responses |
| Motivation | 4 | Autonomy + competence + relatedness |
| Cognitive Biases | 10 | Defaults persist; first impressions anchor |
| Persuasion | 9 | Trust before ask; prove before promise |
| Emotion | 6 | Beautiful feels easier; delight earns loyalty |
| Ethics | 3 | Bright line between persuasion and manipulation |

Total: **65 principles** — see `knowledge/principles.md` for the complete database with definitions and design implications.

---

## Anti-Patterns (Never Do)

- **Fake scarcity counters** — if it's not real, don't show it
- **Confirmshaming** — "No, I don't want to save money" is manipulative
- **Hidden costs at checkout** — the #1 cause of cart abandonment
- **Forced continuity** — hard-to-cancel subscriptions erode all trust
- **Misdirection** — visual tricks to force wrong clicks
- **Fake social proof** — fabricated testimonials or inflated numbers
- **Dark defaults** — pre-checking opt-ins the user didn't ask for
- **Roach motel patterns** — easy to get in, impossible to get out

---

## Source

Principles derived from NN/g's Psychology for UX study guide (112 resources across 11 categories), adapted into actionable design patterns. Academic foundations: Kahneman (Prospect Theory), Norman (Emotional Design), Cialdini (Influence), Hick, Fitts, Miller, Zeigarnik.
