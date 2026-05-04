# Conversation Trigger Rule

When the user starts a request with "Show me ...", treat it as a request to use the `show-me-infographic` skill.

Expected output:
1. Decide whether the best result should be static, interactive, motion-based, photo-led, map-led, chart-led, diagram-led, or mixed media.
2. For real-world, visual, current, factual, local, historical, cultural, product, place, or person topics, gather web/file/source references before designing.
3. Convert sources into visual entities: locations, landmarks, people, dates, quantities, routes, objects, relationships, and evidence.
4. For place/geography topics, default to map-led, photo-led, landmark-led, route-led, orientation-led, or identity-sheet visuals.
5. If the visual looks like a map, choose real map mode or clearly labelled schematic mode.
6. Use images, maps, charts, archive material, official/local details, textures, colours, and typography cues when they would make the result clearer or more fitting.
7. Apply `frontend-design` as a supporting design-quality guideline.
8. Choose a topic-specific art direction, not a fixed brand.
9. Build the visual from topic-native facts, imagery, motifs, colours, layout references, and relationships.
10. Use interactivity only when it improves understanding.
11. Place concise educational explanation and source notes below or beside the visual when useful.
12. Render and inspect the visual before finalizing when the environment allows it.

Failure condition:
- Do not reuse the same layout, slider premise, physics-style simulation, dark monotone palette, or generic canvas composition for unrelated topics.
- Do not rely on labels alone to make a generic visual feel relevant.
- Do not make fake SVG-looking maps/diagrams when real references, photos, maps, charts, or editorial design would communicate better.
- Do not force interactivity when a static infographic would be stronger.
- Do not make card-heavy dashboards, boxed control rails, fake canvas scenes, or generic dark neon layouts by default.
- If the title can be swapped for another unrelated topic and the design still works, the output has failed.
- If the user cannot understand the main subject and takeaway in five seconds, the output has failed.
- Reject label overlap, cramped text, clipped content, large dead zones, and unclear hierarchy.
- Do not let Canvas/SVG pass as decorative filler for real-world overviews.
