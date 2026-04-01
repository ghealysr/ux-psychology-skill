# Contributing

Thanks for wanting to improve the UX Psychology Skill. Here's how to do it well.

## Adding a New Principle

Every principle must meet these criteria:

1. **Published academic backing** — peer-reviewed research, NN/g studies, or foundational texts (Kahneman, Norman, Cialdini, etc.). Blog posts and opinion pieces don't count.
2. **One-line definition** — if you can't explain it in one sentence, it's not distilled enough.
3. **Design implication** — a concrete "do this" statement, not abstract theory.
4. **Page-type mapping** — at least one page type where this principle applies most.
5. **Ethics check** — the principle must have a clear ethical application. If it only works through manipulation, it doesn't belong here.

### Where to add it

1. `knowledge/principles.md` — full definition with the `→` design implication format
2. `knowledge/data/principles.csv` — machine-readable row (Category, Principle, Definition, Design Implication, Weight)
3. `knowledge/page-prescriptions.md` — add to relevant page type(s)
4. `knowledge/data/page-mappings.csv` — if it changes a page type's top 5

### Format

In `principles.md`:
```
**Principle Name** — One-line definition.
→ Design implication: concrete action to take.
```

In `principles.csv`:
```
Category,Principle Name,One-line definition,Design implication,Weight
```

Weight must be one of: `Critical`, `High`, `Medium`, `Low`.

## Adding a Code Example

Code examples go in the SKILL.md under "Code-Level Implementation Examples." Each must include:

1. **Before** — the common/default implementation
2. **After** — the psychology-informed implementation
3. **Why** — 2-3 sentences explaining the principle at work

Use plain HTML or React/JSX. Keep examples minimal — show only what's relevant to the principle.

## Reporting Issues

- **Incorrect principle** — if a definition is wrong or the design implication is misleading, open an issue with the correct information and a source.
- **Missing page type** — suggest new page types with at least 3 relevant principles.
- **Anti-pattern additions** — suggest new anti-patterns with a real-world example of harm.

## Style

- Direct, not academic. Write for developers, not researchers.
- One-line definitions. If you need a paragraph, it's a knowledge article, not a principle.
- Concrete over abstract. "Use a progress bar" beats "leverage the incompleteness heuristic."
- Ethics matter. If you're unsure whether something crosses the line, it probably does.
