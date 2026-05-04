# Conversation Trigger Rule

When the user starts a request with "Show me ...", treat it as a request to use the `show-me-infographic` skill.

Expected output:
1. Decide whether the best result should be static, interactive, motion-based, photo-led, map-led, chart-led, diagram-led, or mixed media.
2. For real-world, visual, current, factual, local, historical, cultural, product, place, or person topics, gather web/file/source references before designing.
3. Use images, maps, charts, archive material, official/local details, textures, colours, and typography cues when they would make the result clearer or more fitting.
4. Apply `frontend-design` as a supporting design-quality guideline.
5. Choose a topic-specific art direction, not a fixed brand.
6. Build the visual from topic-native facts, imagery, motifs, colours, layout references, and relationships.
7. Use interactivity only when it improves understanding.
8. Place concise educational explanation and source notes below or beside the visual when useful.

Failure condition:
- Do not reuse the same layout, slider premise, physics-style simulation, dark monotone palette, or generic canvas composition for unrelated topics.
- Do not rely on labels alone to make a generic visual feel relevant.
- Do not make fake SVG-looking maps/diagrams when real references, photos, maps, charts, or editorial design would communicate better.
- Do not force interactivity when a static infographic would be stronger.
- Do not make card-heavy dashboards, boxed control rails, fake canvas scenes, or generic dark neon layouts by default.
- If the title can be swapped for another unrelated topic and the design still works, the output has failed.
