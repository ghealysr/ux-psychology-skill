# UX Psychology Skill for Claude Code

> Turn behavioral psychology research into actionable design decisions. 69 principles from NN/g, Kahneman, Norman, and Cialdini — mapped to specific page types and components.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## What This Does

When you're building a landing page, pricing page, onboarding flow, or any UI where user behavior matters — this skill surfaces the 3-5 most relevant psychology principles and tells you how to apply them.

It's an **advisory layer**, not a directive. It informs design decisions without overriding your creative judgment, brand identity, or accessibility requirements.

**This is NOT a dark patterns toolkit.** Every principle is framed for ethical application. Manipulation techniques are explicitly listed as anti-patterns.

## Quick Start

### Install

```bash
# Clone into your Claude Code skills directory
cd ~/.claude/skills
git clone https://github.com/nuclearmarmalade/ux-psychology-skill.git ux-psychology
```

Or for a project-specific install:

```bash
cd your-project/.claude/skills
git clone https://github.com/nuclearmarmalade/ux-psychology-skill.git ux-psychology
```

### Use

In Claude Code, just ask:

```
"What psychology principles apply to my pricing page?"
"Review this homepage through a psychology lens"
"Design a conversion sequence for newsletter signups"
```

The skill activates automatically when you're working on pages, components, or flows where user behavior matters.

## What's Inside

### 69 Principles Across 11 Categories

| Category | Principles | Core Insight |
|----------|-----------|--------------|
| Attention | 4 | Users see less than you think |
| Gestalt | 8 | Visual grouping drives comprehension |
| Memory | 12 | Recognition beats recall; chunk everything |
| Sensemaking | 3 | Mental models shape expectations |
| Decision Making | 5 | Fewer choices, clearer outcomes |
| Motor/Interaction | 3 | Big targets, fast responses |
| Motivation | 4 | Autonomy + competence + relatedness |
| Cognitive Biases | 10 | Defaults persist; first impressions anchor |
| Persuasion | 12 | Trust before ask; prove before promise |
| Emotion | 6 | Beautiful feels easier; delight earns loyalty |
| Ethics | 3 | Bright line between persuasion and manipulation |

### Page-Type Prescriptions

Pre-built psychology recommendations for 10 common page types:

- **Homepage / Landing Page** — First impressions, anchoring, social proof
- **Pricing / Subscription** — Anchoring, loss aversion, default effect
- **Picks / Data Dashboard** — Chunking, spatial memory, satisficing
- **Onboarding / Sign-Up** — Progressive commitment, cognitive load, Zeigarnik
- **About / Trust Page** — Authority, hierarchy of trust, transparency
- **Interactive Tools** — Self-determination, flow state, immediate feedback
- **E-commerce Product** — Scarcity, social proof, loss aversion
- **SaaS Feature Page** — Peak-end rule, progressive disclosure, anchoring
- **Blog / Content** — Serial position, information scent, curiosity gap
- **Settings / Account** — Default effect, recognition over recall, error prevention

### Anti-Patterns (Explicitly Banned)

- Fake scarcity counters
- Confirmshaming ("No, I don't want to save money")
- Hidden costs at checkout
- Forced continuity (hard-to-cancel subscriptions)
- Misdirection (visual tricks for wrong clicks)
- Fake social proof (fabricated testimonials)

## How It Weighs Against Other Skills

Psychology principles are **one input among many**. The hierarchy:

1. **Brand identity and creative vision** (highest)
2. **Accessibility and usability** (non-negotiable)
3. **Technical quality** (performance, SEO, responsive)
4. **Psychology principles** (this skill — subtle influence)

If a psychology principle conflicts with good design, good design wins.

## File Structure

```
ux-psychology/
├── SKILL.md                          # Claude Code skill definition
├── README.md                         # This file
├── LICENSE                           # MIT License
├── knowledge/
│   ├── principles.md                 # All 69 principles with definitions
│   ├── page-prescriptions.md         # Page-type → principle mappings
│   └── data/
│       ├── principles.csv            # Machine-readable principle database
│       └── page-mappings.csv         # Page-type mapping data
├── patterns/
│   └── conversion-sequences.md       # Common conversion flow patterns
└── examples/
    ├── saas-landing-review.md        # Example: SaaS landing page review
    ├── ecommerce-checkout-review.md  # Example: E-commerce checkout review
    └── sports-subscription-review.md # Example: Sports subscription review
```

## Academic Foundations

This skill synthesizes research from:

- **NN/g (Nielsen Norman Group)** — Psychology for UX study guide (112 resources)
- **Daniel Kahneman** — Prospect Theory, loss aversion, anchoring
- **Don Norman** — Emotional Design, three levels of processing
- **Robert Cialdini** — Influence: reciprocity, social proof, scarcity, authority, commitment, liking
- **George Miller** — The Magical Number Seven (chunking)
- **Bluma Zeigarnik** — Zeigarnik Effect (incomplete tasks)
- **Paul Fitts** — Fitts's Law (target size and distance)
- **William Hick** — Hick's Law (choice paralysis)

## Contributing

PRs welcome. If you want to add a principle:

1. Ensure it has published academic backing (not just blog posts)
2. Include: principle name, one-line definition, design implication
3. Map it to at least one page type in `page-prescriptions.md`
4. Add it to `principles.csv` for machine-readability

## License

MIT — use it however you want. Attribution appreciated but not required.

## Author

Built by [Nuclear Marmalade](https://nuclearmarmalade.com) as part of the Buzzy Bets web design system. Released publicly because nobody should have to reinvent the wheel on behavioral psychology for web design.
