# Skill Registry

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
2. Use Canvas 2D for the main visual.
3. Use the sleek dark scientific infographic brand.
4. Place the interactive visual first.
5. Put concise educational explanation below the visual.
6. Do not use image generation.
