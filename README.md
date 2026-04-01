# UX Psychology Skill for Claude Code

65 behavioral psychology principles → actionable design decisions.

Drop this skill into Claude Code and it will surface the 3-5 most relevant psychology principles for whatever you're building — landing pages, pricing, onboarding, dashboards, checkout flows — with specific implementation guidance and code examples, not abstract theory.

Built on NN/g, Kahneman, Norman, and Cialdini. Ethics-first — dark patterns are explicitly documented as anti-patterns.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## What This Does

You built a page. It looks good. But is it *working*?

This skill is the psychology review layer. After you design or build any UI where user behavior matters — run it through this skill. It identifies which behavioral principles are at work (intentionally or not), surfaces missed opportunities, flags anti-patterns, and recommends specific changes down to the code level.

**This is NOT a dark patterns toolkit.** Every principle is framed for ethical application. Manipulation techniques are explicitly listed as anti-patterns.

## Quick Start

### Install

```bash
# Clone into your Claude Code skills directory
cd ~/.claude/skills
git clone https://github.com/Nuclear-Marmalade/ux-psychology-skill.git ux-psychology
```

Or for a project-specific install:

```bash
cd your-project/.claude/skills
git clone https://github.com/Nuclear-Marmalade/ux-psychology-skill.git ux-psychology
```

Or manually: copy the entire directory into `~/.claude/skills/ux-psychology/` or `your-project/.claude/skills/ux-psychology/`. Claude Code will discover the `SKILL.md` automatically.

### Use

In Claude Code, just ask:

```
"What psychology principles apply to my pricing page?"
"Review this homepage through a psychology lens"
"Design a conversion sequence for newsletter signups"
"I just built a checkout flow — what am I missing psychologically?"
"Review my onboarding for cognitive load issues"
```

The skill activates automatically when you're working on pages, components, or flows where user behavior matters.

## What's Inside

### 65 Principles Across 11 Categories

| Category | Principles | Core Insight |
|----------|-----------|--------------|
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

### Self-Contained SKILL.md

The `SKILL.md` works on its own — it includes inline page-type prescriptions, a decision process, and code-level implementation examples. Claude Code doesn't need to read any other file to give you useful output. The `knowledge/` directory provides depth when you need it.

### Page-Type Prescriptions

Pre-built psychology recommendations for 11 common page types:

- **Homepage / Landing Page** — First impressions, anchoring, social proof
- **Pricing / Subscription** — Anchoring, loss aversion, default effect
- **Data Dashboard** — Chunking, spatial memory, satisficing
- **Onboarding / Sign-Up** — Progressive commitment, cognitive load, Zeigarnik
- **About / Trust Page** — Authority, hierarchy of trust, transparency
- **Interactive Tools** — Self-determination, flow state, immediate feedback
- **E-commerce Product** — Scarcity, social proof, loss aversion
- **SaaS Feature Page** — Peak-end rule, progressive disclosure, anchoring
- **Blog / Content** — Serial position, information scent, curiosity gap
- **Checkout** — Cognitive load, transparency, trust signals
- **Settings / Account** — Default effect, recognition over recall, reversibility

### Code-Level Examples

The skill includes before/after code for key principles:
- **Anchoring** — pricing tier layout that creates a visual anchor
- **Loss Aversion** — CTA copy that frames around what users lose
- **Zeigarnik Effect** — stepped onboarding with progress indication
- **Cognitive Load** — guest checkout vs. forced account creation

### Anti-Patterns (Explicitly Banned)

- Fake scarcity counters
- Confirmshaming ("No, I don't want to save money")
- Hidden costs at checkout
- Forced continuity (hard-to-cancel subscriptions)
- Misdirection (visual tricks for wrong clicks)
- Fake social proof (fabricated testimonials)
- Dark defaults (pre-checked opt-ins)
- Roach motel patterns (easy in, impossible out)

## How It Weighs Against Other Concerns

Psychology principles are **one input among many**. The hierarchy:

1. **Brand identity and creative vision** (highest)
2. **Accessibility and usability** (non-negotiable)
3. **Technical quality** (performance, SEO, responsive)
4. **Psychology principles** (this skill — subtle influence)

If a psychology principle conflicts with good design, good design wins.

## File Structure

```
ux-psychology/
├── SKILL.md                          # Skill definition (self-contained)
├── README.md                         # This file
├── LICENSE                           # MIT License
├── CHANGELOG.md                      # Version history
├── CONTRIBUTING.md                   # How to add principles
├── knowledge/
│   ├── principles.md                 # All 65 principles with definitions
│   ├── page-prescriptions.md         # Page-type → principle mappings
│   └── data/
│       ├── principles.csv            # Machine-readable principle database
│       └── page-mappings.csv         # Page-type mapping data
├── patterns/
│   └── conversion-sequences.md       # Common conversion flow patterns
└── examples/
    ├── saas-landing-review.md        # Example: SaaS landing page review
    ├── ecommerce-checkout-review.md  # Example: E-commerce checkout review
    └── subscription-review.md        # Example: Subscription conversion review
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

## License

MIT — use it however you want. Attribution appreciated but not required.

## Author

Built by [Glen Healy](https://x.com/NukeGlen) at [Nuclear Marmalade](https://nuclearmarmalade.com) — a one-person AI design and implementation agency.

Released under MIT because behavioral psychology shouldn't be gatekept behind expensive consultancies.
