---
name: show-me-infographic
description: Use this skill when the user asks "show me...", "visualize...", "explain visually...", "make an infographic about...", or asks for an educational visual about any topic. Create a researched, topic-fitted, visually strong infographic or explainer. Choose static, interactive, photographic, editorial, diagrammatic, map-based, timeline, simulation, or mixed-media form based on the topic. Do not default to a fixed brand, layout, dark theme, SVG/canvas diagram, card layout, or interactivity.
---

# Show Me Infographic Skill

## Purpose

Create an excellent educational visual for the user's topic. The output should feel designed for that exact subject, audience, place, era, culture, discipline, and learning goal.

The skill must not impose a house style. There is no required monotone brand, no required dark technical layout, no required Canvas/SVG diagram, no required timeline, and no required interactivity. A Sasolburg infographic should not look like a physics simulation. A bias explainer should not look like a map. A town, person, place, product, event, artwork, anatomy topic, equation, or social concept can each need a completely different visual language.

The rule is: **topic first, reference first, art direction second, implementation third.**

If the result would still make sense after replacing the title with a different unrelated topic, it is a failed result.

## Supporting Skills and Domains

Apply `.agents/skills/frontend-design/SKILL.md` as a supporting design-quality guideline when creating coded visuals or interfaces.

Also apply relevant domain/tool guidance:
- `domains/research-and-citations.md` for factual or current topics,
- `domains/file-research.md` when user-provided files are involved,
- `domains/simulations-and-modeling.md` for actual simulations,
- `tools/ocr-vision-pipeline.md` when extracting visual text from images/scans,
- `tools/file-research-pipeline.md` when building from documents,
- `tools/simulation-design.md` only when a simulation is genuinely the right form.

These support the skill. They do not override the visual goal.

## Trigger

Use this skill when the user says or clearly means:
- "Show me ..."
- "Visualize ..."
- "Explain visually ..."
- "Make an infographic about ..."
- "Create an interactive explainer for ..."
- "Make a visual guide to ..."

Do not use this skill when the user asks only for a normal text explanation.

## Research and Reference Rule

Before making the visual, decide whether references are needed. Most real-world topics need references.

Use web or supplied sources when:
- the topic is a place, person, organization, current event, product, artwork, building, disease, law, public issue, or anything factual,
- visual identity matters,
- photos, maps, charts, logos, official colours, historical imagery, or source facts would improve the infographic,
- the user asks about a specific real thing, such as "Show me Sasolburg."

For real-world topics, do not treat references as optional decoration. Gather enough source material to understand the visual world of the topic before deciding the layout. This can include source facts, reference images, maps, material textures, typography cues, colour cues, archive material, official pages, local news, data tables, or diagrams.

When web access is available, browse for current or specific real-world topics unless the user explicitly says not to. If web access is unavailable, say so and use only the supplied context or stable general knowledge.

For real-world places, prefer:
- maps or geographic context,
- real photographs where allowed and useful,
- official/local sources,
- historical context,
- recognizable local industries, landmarks, architecture, natural features, colours, textures, and typography cues.

For Sasolburg specifically, a better direction might be an editorial South African industrial-town feature, Vaal River geography, Sasol/coal-to-liquids history, Free State/Gauteng boundary context, archival or modern industrial photography, map fragments, newspaper-like typography, and a stronger sense of place. A fake neon SVG map with generic nodes is a failure.

The Sasolburg failure pattern to avoid:
- dark neon background,
- fake vector river and fake town nodes,
- generic timeline slider,
- boxed control rail,
- labels doing all the relevance work,
- no real photo, map, archive, industrial, civic, or local visual reference.

## Output Mode Selection

Choose the output mode that best serves the topic:

| Topic need | Better output mode |
|---|---|
| Real place, person, object, product, or event | researched editorial infographic, photo-led layout, map/photo/text hybrid |
| Historical story | timeline, archive/newspaper aesthetic, annotated images, cause-effect bands |
| Scientific or mechanical process | diagram, simulation, staged animation, graph plus object |
| Abstract concept | scenario comparison, evidence map, metaphor only if carefully chosen |
| Data-heavy question | chart-first infographic with clear scales and source notes |
| Anatomy or clinical topic | labelled illustration/cross-section with accurate source-based details |
| Math concept | graph/geometric construction/step transformation |
| Quick conceptual overview | static infographic may be better than interactivity |
| User needs exploration or parameter change | interactive model or simulation |

Static is allowed. Interactive is allowed. Motion is allowed. Photographic/editorial is allowed. Mixed media is allowed. Choose deliberately.

Default to static/editorial when the prompt asks for a place, event, biography, history, culture, public issue, or overview unless manipulation is central to understanding. Default to simulation only when variables, physics, mechanics, math, or process dynamics are central.

## Form Rules

Do not default to:
- dark monotone background,
- cyan/purple accents,
- Inter/system fonts,
- one huge rounded rectangle,
- nested cards,
- bento/card grids,
- right-side control rail,
- generic toggles/sliders,
- generic dashboard readouts,
- fake SVG-looking icons,
- fake canvas scenes,
- fake maps,
- abstract glowing dots,
- generic arrows and nodes,
- repetitive "read the model" panels,
- card-heavy dashboards.

Avoid SVG/canvas-style visual filler unless that medium is truly right and the artwork is genuinely good. If a topic needs visual richness, use high-quality photographs, texture, maps, charts, collage, typography, or custom illustration instead of sterile placeholder geometry.

Do not use cards as the default layout. If grouping is needed, use editorial sections, annotated bands, callout labels, overlaid captions, margins, columns, timelines, or map/photo panels. Use cards only when they are clearly the best structure.

## Art Direction

Choose a specific art direction for each prompt. Examples:
- newspaper editorial,
- archival documentary,
- museum wall graphic,
- field guide,
- industrial technical poster,
- travel magazine spread,
- scientific journal figure,
- classroom wall chart,
- civic data story,
- luxury product explainer,
- comic-strip sequence,
- blueprint,
- atlas/map plate,
- clinical teaching plate.

The art direction must fit the topic. It should vary across generations. Do not converge on one recurring look.

Before committing to a layout, consider at least two materially different art directions and reject the weaker one. Examples: "newspaper spread vs. map plate" for a town, "lab notebook vs. animated apparatus" for a science process, "courtroom evidence board vs. social media feed analysis" for bias.

## Visual Quality Bar

The visual should look intentional, not generated from a template.

Good outputs:
- have a clear composition,
- use visual hierarchy,
- use typography that fits the subject,
- use colour with purpose and energy,
- include real references or source-grounded details when useful,
- have whitespace and density under control,
- make the topic recognizable before reading every label,
- contain details that would be wrong in an unrelated topic.

Bad outputs:
- look like the same infographic with a new title,
- use generic vector shapes where real visual material would be better,
- add interactivity for no reason,
- use flat monotone palettes for every topic,
- make ugly fake maps or fake diagrams,
- use stock dashboard/card layout for a visual story,
- hide the topic behind abstract decoration,
- feel like a dashboard instead of an infographic,
- use controls that only change labels.

## Topic-Fit Contract

Before implementing, define internally:
- learning goal,
- audience,
- source/reference needs,
- best output mode: static, interactive, motion, photo-led, diagram-led, map-led, chart-led, or mixed,
- visual art direction,
- topic-native objects/details,
- topic-native relationships,
- what would make the design ugly or wrong for this topic.

If the first design idea would also work for five unrelated topics, reject it.

## Interactivity and Motion

Interactivity is optional.

Use interactivity only when it lets the user explore a meaningful variable, compare views, scrub time, reveal layers, or test a cause-effect relationship.

Do not add sliders, toggles, or animated dots just to appear interactive.

If the interaction can be removed without losing meaning, remove it and make a stronger static composition.

Movement is allowed when it improves the piece:
- subtle page-load reveal,
- animated map route,
- time scrubber,
- before/after transition,
- process motion,
- hover/reveal labels.

Avoid motion that distracts, flickers, or makes labels hard to read.

## Implementation Rules

Choose the best implementation for the visual:
- HTML/CSS for editorial/static infographic layouts,
- React for structured interactive artifacts,
- Canvas for custom simulations or dynamic drawing,
- SVG only when it is truly the right medium and not ugly filler,
- external images when allowed, sourced, and relevant,
- CSS motion when it adds life without overengineering.

For editorial/static outputs, prefer strong HTML/CSS composition with images, typography, texture, captions, charts, and annotation before reaching for canvas.

The artifact must be self-contained where possible and responsive. If using external images, use stable URLs and provide alt text. Do not hotlink questionable sources when source reliability or licensing is unclear; use official/public-domain/clearly usable sources where possible.

## Source Honesty

If facts or visuals are sourced:
- cite or link the source when possible,
- distinguish source facts from design interpretation,
- do not invent local details,
- do not fabricate image sources,
- avoid exact claims without evidence.

## Required Workflow

1. Parse the topic and learning goal.
2. Decide whether research/web/file references are needed. Use them when they would materially improve factual accuracy or visual quality.
3. For real-world topics, gather source/reference material before designing.
4. Choose output mode: static, interactive, motion, photo-led, diagram-led, map-led, chart-led, or mixed.
5. Consider at least two different art directions and choose the one that best fits the topic.
6. Gather topic-native facts, imagery ideas, visual motifs, colours, textures, and layout references.
7. Design the infographic around those references.
8. Build the artifact or visual output.
9. Verify facts, sources, layout, responsiveness, readability, and whether the design is actually good.

## Final Gate

Before finalizing, reject and redesign if:
- it has the old dark/cyan/purple monotone technical look by default,
- it uses fake SVG-looking elements where better imagery or layout is possible,
- it forces interactivity when static would be stronger,
- it lacks real references for a real-world topic,
- the layout feels like the same repeated template,
- the design is ugly, cramped, illegible, generic, or unrelated to the topic,
- the output is mostly cards, controls, labels, and empty geometry,
- the topic would be more effectively shown through photos, maps, charts, or editorial design and those were not considered.

The final result should feel like someone thought: "What is this topic, what would make it visually memorable, and what medium makes it clear?"
