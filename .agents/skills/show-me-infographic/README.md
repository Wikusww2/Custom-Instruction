# show-me-infographic

This is an OpenAI/Codex-style skill package.

## Main file

- `SKILL.md`
- `TRIGGER_RULE.md`

## Design behavior

The skill should keep a high visual quality bar, but it must not keep one fixed brand. It should change the visual model, layout, medium, imagery, typography, colours, and interaction level to fit the topic.

It also uses `frontend-design` as a supporting design-quality guideline. That improves aesthetic direction and polish, but does not replace the show-me skill's topic-first requirements.

For real-world topics, the skill should actively use web/file/source references, maps, real imagery, editorial layouts, charts, and other visual material when those would improve the result. Places, people, products, public issues, history, culture, and current topics should not be designed from generic memory alone when browsing or supplied files are available.

It should not default to fake SVG-style diagrams, fake canvas scenes, dark monotone palettes, cards, boxed control rails, or unnecessary interactivity. Static editorial infographics are often better than interactive toys. Interactivity should appear only when it helps the user understand a variable, comparison, process, or timeline.

The core test is simple: if the title can be swapped for an unrelated topic and the design still works, the design failed.

The second core test is usefulness: the user should understand the main subject, context, and takeaway within five seconds, before reading long explanatory paragraphs.

For towns, cities, countries, buildings, landmarks, campuses, and regions, the skill should default to map-led, photo-led, landmark-led, route-led, orientation-led, or identity-sheet visuals. Map-like graphics must be either geographically faithful or clearly labelled as schematic.

Generated artifacts should be visually inspected before finalizing when possible. Reject overlap, cramped labels, clipped content, large dead zones, unclear hierarchy, and Canvas/SVG filler.

## Trigger phrases

Use this skill for:
- “Show me ...”
- “Visualize ...”
- “Explain visually ...”
- “Make an interactive infographic about ...”

## Installation

To install as a standalone skill, zip this folder so the ZIP contains one top-level folder named `show-me-infographic` with `SKILL.md` inside it.
