---
name: show-me-infographic
description: Use this skill when the user asks “show me…”, “visualize…”, “explain visually…”, “make an interactive infographic about…”, or asks for a code-rendered educational visual about any topic. Generate a consistent, sleek, dark, minimal, interactive infographic with topic-specific visual reasoning and explanatory text below it. Do not use image generation.
---

# Show Me Infographic Skill

## Purpose

Create a consistent, code-rendered educational infographic for any topic the user asks to “show me.” Preserve one recognizable visual brand while adapting the diagram, layout, controls, and visual metaphor to the subject.

The goal is not to reuse the same diagram, page composition, control set, or premise every time. The goal is to preserve design language, interaction quality, information hierarchy, and explanatory style across different domains while changing the visual logic to fit the topic.

The core rule is: same brand, different visual thinking. A physics concept, a biological structure, a social concept, a mathematical transformation, and a historical event should not look like variations of the same circuit, wave, slider, or canvas template.

## Trigger

Use this skill when the user says or clearly means:
- “Show me ...”
- “Visualize ...”
- “Explain visually ...”
- “Make an interactive infographic about ...”
- “Create an interactive explainer for ...”

Do not use this skill when the user asks for AI image generation or only wants a normal text explanation.

## Core Output Rule

Generate a visual, interactive infographic first, then place the explanation below it.

Preferred output:
1. A single rendered React component.
2. A code-generated topic-specific visual as the dominant first element.
3. Controls placed where they best support the visual, such as below, beside, above, inside a side rail, or as a compact stepper.
4. Data readouts, labels, short facts, or qualitative status indicators linked to the controls.
5. Clear explanatory text below the visual.

Do not use image generation. Do not merely describe the infographic unless rendering is impossible.

## Visual Brand System

Use a sleek, minimal, dark educational-science look:
- dark matte background,
- clean scientific diagram,
- high-contrast white headings,
- muted grey labels,
- restrained accent colours,
- thin technical lines,
- soft minimal motion,
- precise spacing,
- no decorative clutter.

Use one coherent infographic page, not a card dashboard. The page structure may change to fit the topic.

Required content, with flexible placement:
1. Header with small uppercase eyebrow label, strong title, and one interaction sentence.
2. Dominant topic-specific visual area.
3. Controls only when they clarify the concept.
4. Readouts, annotations, legends, or state labels where appropriate.
5. Explanation underneath.

Allowed layout archetypes:
- single-stage simulation for one changing system,
- split comparison for before/after or competing interpretations,
- side-by-side graph plus object view for measurable concepts,
- timeline track for historical or developmental sequences,
- layered cross-section for anatomy, geology, devices, or systems,
- network map for relationships, feedback loops, or influence,
- matrix or spectrum for classification, tradeoffs, or bias patterns,
- guided stepper for processes where sequence matters,
- zoom lens or nested scale view for microscopic, cosmic, or hierarchical topics.

Do not default to a header, one large rectangular canvas, horizontal controls, three readout boxes, and paragraphs every time. Use that composition only when it is the best fit for the topic.

Avoid:
- card-based layouts,
- dashboard clutter,
- unrelated icons,
- generic templates,
- stock image aesthetics,
- beige, cream, warm terracotta, off-white, or muted deep green palette defaults,
- SVG unless explicitly requested.

Default palette:
- Page background: near-black or neutral-950.
- Main text: neutral-100 or white.
- Secondary text: neutral-400 to neutral-500.
- Divider lines: neutral-800.
- Technical lines: neutral-600 to neutral-700.
- Active accent: choose intelligently from cyan, blue, violet, amber, red, or topic-appropriate spectral colours.

Use colour semantically. Keep non-data elements neutral. Reserve bright colour for active, moving, selected, or important elements.

Use system UI or Inter-style typography. Use bold sparingly.

## Technical Implementation Rules

Default to a single React component with Canvas 2D for the main infographic.

Preferred stack:
- React,
- Tailwind CSS utility classes,
- HTML Canvas 2D,
- React state,
- `useMemo`, `useRef`, and `useEffect`,
- `requestAnimationFrame` for meaningful animation.

The component must:
- be self-contained,
- default export one React component,
- avoid unnecessary dependencies,
- use meaningful variable names,
- keep constants near the top,
- be responsive,
- include accessible labels for controls,
- avoid dead controls.

The code should expose the chosen concept model in clear constants. Examples:
- process phases for a sequence,
- material properties for engineering,
- anatomical layers for biology,
- evidence weights for bias or judgement,
- nodes and links for systems,
- bins and distributions for statistics,
- events and causal links for history.

Do not begin from a prior topic's implementation and rename labels. Reusing helper functions is fine; reusing the same visual premise is not.

## Interactivity Rules

Add interactivity only when it improves understanding.

Good controls:
- sliders for continuous variables,
- toggles for modes or overlays,
- material or condition selectors,
- play/pause animation,
- step-through sequence controls,
- click-to-select regions,
- draggable handles when they clarify cause and effect.

Every control must update at least two of:
- main visual,
- numeric readout,
- label,
- explanatory sentence,
- highlighted region,
- animation state.

Prefer 1 to 4 strong controls over many weak controls.

Controls must match the domain. Use a voltage slider for a circuit, a strain slider for tensile strength, a wavelength slider for light, a phase selector for mitosis, an evidence-weight slider for bias, and a timeline scrubber for history. Do not reuse a generic "strength" slider when the concept has a more truthful variable.

## Animation Rules

Use subtle animation only when it clarifies change, flow, force, motion, sequence, or transformation.

Acceptable animation:
- moving wave or particle,
- flowing current or fluid,
- cycling process step,
- stress increasing on a material,
- pulsing highlight,
- gradual deformation,
- time progression.

Avoid distracting motion, flashing, and decorative animation. Provide pause/resume if animation is continuous.

## Choose the Best Visual Model

Do not force every topic into the same visual pattern. First identify what the user needs to see and what kind of thing the topic is.

Before coding, make an internal visual brief with these decisions:
1. Domain: physical, biological, mathematical, social, historical, procedural, systemic, comparative, scale-based, or abstract.
2. Core invisible idea: flow, force, structure, sequence, transformation, distribution, tradeoff, cause-effect, hierarchy, feedback, uncertainty, or perspective.
3. Visual grammar: arrows, layers, axes, particles, fields, curves, maps, timelines, matrices, lenses, balances, trees, or networks.
4. Layout archetype: choose from the layout list above or create a better one.
5. Control model: choose only controls that manipulate the real conceptual variables.
6. Failure check: name one visual metaphor that would be wrong for this topic and avoid it.

| Topic type | Best visual model | Possible controls |
|---|---|---|
| Mechanism/process | flow diagram, causal chain, animated sequence | stepper, speed, reveal labels |
| Physical law/engineering | parameterized simulation, vectors, graph, specimen diagram | sliders, material selector, overlay toggle |
| Anatomy/biology | labelled cross-section, layers, pathway, zoomed region | layer toggles, pathology toggle, stage selector |
| Chemistry | particle model, reaction pathway, energy diagram | concentration, temperature, phase toggle |
| Mathematics | graph, geometric construction, transformation view | parameter sliders, formula toggle |
| Statistics | distribution, sampling animation, confidence region | sample size, mean, variance |
| Timeline/history | horizontal timeline, cause-effect map | era selector, theme highlight |
| Comparison | aligned scales, matrix, before/after | category selector, sort mode |
| System/network | nodes, flows, feedback loops | isolate subsystem, toggle flows |
| Scale/spectrum | logarithmic scale, gradient, zoom window | marker, scale mode |
| Abstract/social concept | evidence map, balance, lens/filter, spectrum, causal map, scenario comparison | bias strength, evidence mix, perspective toggle, mitigation stepper |
| Ethics/reasoning | decision tree, stakeholder map, claim-evidence-warrant view | assumption toggle, evidence quality, consequence horizon |
| Language/concept definition | semantic map, contrast pairs, examples/non-examples, boundary cases | reveal layers, compare cases, ambiguity slider |

Examples:
- Tensile strength: specimen bar pulled from both ends, stress-strain curve, strain slider, material selector, elastic/yield/ultimate/fracture labels.
- Mitosis: cell diagram changing by phase, chromosomes separating, phase selector, spindle fibre toggle.
- Optic nerve cupping: optic disc cross-section, top-view cup-to-disc representation, cup-to-disc ratio slider, rim/RNFL/IOP context.
- Bias: do not make it look like a physics field or generic particle flow. Use an evidence-to-judgement visual: balanced evidence points, a bias lens/filter that weights some evidence more heavily, a neutral reference line, shifted judgement, and a mitigation/checking control. For social bias, use group assumptions versus individual evidence. For data bias, use sampling coverage and missing regions. For cognitive bias, use attention weighting and prior-belief pull.
- Electricity: circuit path, battery potential difference, load, charge/current flow, field direction, resistance, and power readouts.
- Light: wave and ray optics, wavelength, photon energy, refraction/reflection boundary, spectrum marker, medium selector.

For medical topics, keep the explanation educational and avoid diagnosis unless clinical context is supplied and clinical reasoning is requested.

## Anti-Template Rules

The skill fails if it produces a one-shoe-fits-all design.

Reject and redesign before final output when:
- the same layout would work unchanged for the previous unrelated topic,
- the title is the only part that makes the diagram topic-specific,
- the controls are generic instead of concept-specific,
- the visual uses waves, particles, arrows, gauges, or sliders only because they are easy to draw,
- an abstract, social, historical, or reasoning topic is forced into a physics-style simulation,
- a physical mechanism is reduced to a generic metaphor when a direct diagram or simulation is possible,
- the explanation describes relationships that are not visible in the diagram.

Acceptable consistency:
- dark technical brand,
- typography,
- spacing discipline,
- label style,
- motion restraint,
- explanation style.

Unacceptable sameness:
- same canvas composition,
- same horizontal control strip,
- same three readout boxes,
- same moving dots or arrows,
- same "change one strength slider and watch something shift" premise,
- same rectangular framed stage for every topic.

## Knowledge and Research Rules

Before generating the infographic, decide whether factual verification is needed.

Use reliable sources when:
- the topic is medical, legal, financial, safety-related, or high-stakes,
- the user asks for current information,
- numerical constants, ranges, standards, or classifications matter,
- the topic is niche or unfamiliar.

When facts are uncertain:
- state uncertainty clearly,
- avoid overclaiming,
- mark simplified educational models as simplified.

Never fabricate statistics, thresholds, guidelines, citations, mechanisms, anatomical details, or clinical claims.

## Explanation Below the Visual

The explanation must be concise but substantial.

Recommended structure:
1. Big-picture sentence.
2. Three to five short paragraphs, each starting with a bold key concept.
3. Each paragraph explains what the visual is showing.
4. Tie the explanation to controls when possible.

Use correct terminology. On first mention, write the full term followed by the abbreviation when useful, such as ultimate tensile strength (UTS), intraocular pressure (IOP), retinal nerve fibre layer (RNFL), or deoxyribonucleic acid (DNA).

Include units wherever numeric values appear.

## Required Workflow

1. Parse the prompt: topic, learning goal, scope, domain, and whether controls help.
2. Create the internal visual brief: domain, invisible idea, visual grammar, layout archetype, control model, and wrong-fit metaphor to avoid.
3. Decide the visual metaphor: structure, flow, force, scale, comparison, time, probability, classification, perspective, or evidence weighting.
4. Design the interaction model: only meaningful controls.
5. Build the visual: dark brand, topic-specific geometry, labels near objects, responsive scaling.
6. Write the explanation: what viewer sees, what controls change, key principle, why it matters.
7. Final consistency check: topic match, dynamic layout choice, working controls, correct units, readable labels, meaningful colours, supported claims, explanation matches visual.

## Output Constraints

Do not:
- use image generation,
- output only text,
- create a downloadable file unless requested,
- use a card-heavy layout,
- use unrelated decorative graphics,
- use warm cream/beige/terracotta/off-white/muted deep green default palettes,
- overuse gradients,
- make the diagram childish,
- include meaningless controls,
- reuse a visual premise from an unrelated topic,
- force abstract topics into physical simulations,
- invent facts or fake exactness.

Do:
- render the infographic first when possible,
- keep one strong visual identity,
- adapt the diagram intelligently to the topic,
- choose a layout archetype from the actual concept,
- use dynamic state when helpful,
- keep explanatory text below the visual,
- verify high-stakes or current facts.

## Quality Bar

A successful output passes these tests:
1. If the title were removed, the diagram should still suggest the topic.
2. If controls were removed, the visual should still teach something.
3. If text were removed, the user should still understand the main structure.
4. Outputs should look like one brand family.
5. When the topic changes, the visual metaphor changes while the brand stays consistent.
6. A bias output should not look like a light output, a light output should not look like an electricity output, and neither should look like tensile strength.

## Minimal Starting Template

Use this only as a minimal wiring reference for React, Canvas, state, and resize behavior. It is not a layout template and not a design template. Replace the component state, layout, control placement, readouts, drawing functions, and explanatory structure to fit the topic.

```jsx
import React, { useEffect, useMemo, useRef, useState } from "react";

export default function ShowMeInfographic() {
  const canvasRef = useRef(null);
  const [primaryParameter, setPrimaryParameter] = useState(50);
  const [mode, setMode] = useState("default");
  const [paused, setPaused] = useState(false);

  const derived = useMemo(() => ({
    label: "Derived value",
    value: primaryParameter,
  }), [primaryParameter]);

  useEffect(() => {
    const canvas = canvasRef.current;
    const ctx = canvas.getContext("2d");
    let frameId;
    let t = 0;

    function resize() {
      const dpr = window.devicePixelRatio || 1;
      const rect = canvas.getBoundingClientRect();
      canvas.width = Math.floor(rect.width * dpr);
      canvas.height = Math.floor(rect.height * dpr);
      ctx.setTransform(dpr, 0, 0, dpr, 0, 0);
    }

    function draw() {
      resize();
      if (!paused) t += 0.016;
      ctx.clearRect(0, 0, canvas.clientWidth, canvas.clientHeight);
      // Draw the topic-specific infographic here.
      frameId = requestAnimationFrame(draw);
    }

    draw();
    window.addEventListener("resize", resize);
    return () => {
      cancelAnimationFrame(frameId);
      window.removeEventListener("resize", resize);
    };
  }, [primaryParameter, mode, paused]);

  return (
    <main className="min-h-screen bg-neutral-950 px-5 py-7 text-neutral-100">
      <section className="mx-auto max-w-6xl">
        <header className="mb-5 border-b border-neutral-800 pb-5">
          <p className="mb-1 text-sm font-semibold uppercase tracking-[0.22em] text-neutral-500">
            interactive explainer
          </p>
          <h1 className="text-3xl font-black tracking-tight md:text-4xl">
            Show me [topic]
          </h1>
          <p className="mt-3 max-w-2xl text-base font-medium leading-relaxed text-neutral-400">
            Use the controls to change the key variable and see the visual update.
          </p>
        </header>

        <canvas
          ref={canvasRef}
          className="h-[680px] w-full border-b border-neutral-800 bg-neutral-950"
          aria-label="Interactive infographic"
        />

        <section className="border-b border-neutral-800 py-6">
          {/* Controls go here. */}
        </section>

        <section className="grid gap-5 border-b border-neutral-800 py-6 md:grid-cols-4">
          {/* Readouts go here. */}
        </section>

        <section className="max-w-5xl space-y-5 py-7 text-xl leading-relaxed text-neutral-100">
          <p><strong>Key concept.</strong> Explain what the visual shows.</p>
          <p><strong>Interaction.</strong> Explain what changes when the user moves the controls.</p>
          <p><strong>Why it matters.</strong> Explain the practical or conceptual importance.</p>
        </section>
      </section>
    </main>
  );
}
```

Consistency does not mean sameness. The brand must stay consistent. The visual logic must adapt to the topic.
