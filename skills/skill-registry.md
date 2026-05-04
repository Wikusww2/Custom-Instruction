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
- the user requests a static exported image,
- rendering is impossible and no code artifact is desired.

Expected output:
1. Create a live rendered React artifact when possible.
2. Use Canvas 2D for the main visual when appropriate.
3. Keep the sleek dark scientific infographic brand.
4. Also load `frontend-design` as a supporting guideline because this is design happening in code.
5. Choose a topic-specific visual model, layout archetype, and control model before coding.
6. Prove the visual fit with topic-native objects, variables, and relationships.
7. Place the interactive visual first.
8. Put concise educational explanation below the visual.
9. Do not use image generation.

Quality requirement:
- Consistency means shared brand language, not repeated layouts.
- The skill must not force unrelated topics into the same circuit, wave, slider, readout, or generic physics-style composition.
- A good result should feel designed for the exact topic, not merely relabelled for it.
