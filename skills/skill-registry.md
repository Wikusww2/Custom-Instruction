# Skill Registry

## frontend-design

Path:
- `.agents/skills/frontend-design/SKILL.md`

Use when:
- the task involves design happening in code,
- the user asks to build or improve a web component, page, application, dashboard, game, interactive artifact, visualization, or coded UI,
- layout, styling, typography, colour, motion, controls, interaction states, or visual polish materially affect the result.

Do not use when:
- the user asks only for non-UI backend code,
- the user asks only for prose, data extraction, or non-visual reasoning,
- another skill forbids code output or frontend artifacts.

Expected effect:
1. Choose a clear aesthetic direction from the task context.
2. Avoid generic AI-looking frontend choices.
3. Produce working code with deliberate typography, colour, layout, motion, and responsive behavior.
4. When combined with another skill, act as a design-quality guideline, not as a replacement for that skill's domain logic.

## show-me-infographic

Path:
- `.agents/skills/show-me-infographic/SKILL.md`

Use when the user asks:
- “Show me ...”
- “Visualize ...”
- “Explain visually ...”
- “Make an interactive infographic about ...”
- asks for a code-rendered educational visual about a topic.

Do not use when:
- the user asks for AI image generation,
- the user asks only for a normal text explanation,
- rendering is impossible and no code artifact is desired.

Expected output:
1. Choose the right medium: static, interactive, motion, photo-led, map-led, chart-led, diagram-led, editorial, or mixed.
2. Use web/file/source references before designing real-world, visual, current, local, historical, cultural, product, place, or person topics.
3. Also load `frontend-design` as a supporting guideline because this is design happening in code.
4. Choose a topic-specific art direction and visual model before coding.
5. Prove the visual fit with topic-native objects, imagery, maps, photos, charts, textures, typography cues, variables, relationships, and source-grounded details.
6. Use interactivity only when it improves understanding.
7. Put concise educational explanation below or beside the visual when useful.

Quality requirement:
- Consistency means quality, not repeated layouts or colours.
- The skill must not force unrelated topics into the same circuit, wave, slider, readout, dark monotone palette, SVG/canvas-style map, card layout, control rail, or generic physics-style composition.
- A good result should feel designed for the exact topic, not merely relabelled for it.
- If the title can be swapped for another unrelated topic and the design still works, the output has failed.
