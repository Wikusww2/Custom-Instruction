---
name: show-me-infographic
description: Use this skill when the user asks “show me…”, “visualize…”, “explain visually…”, “make an interactive infographic about…”, or asks for a code-rendered educational visual about any topic. Generate a polished, topic-fitted, interactive infographic with explanatory text below it. Do not use image generation.
---

# Show Me Infographic Skill

## Purpose

Create a code-rendered educational infographic for any topic the user asks to "show me." The result must be visually and conceptually fitted to the topic, not a generic canvas with changed labels.

The skill has two goals:
- preserve a high-quality, polished educational interface,
- change the visual model, layout, controls, and visual language to match the actual topic.

Consistency means quality, clarity, and deliberate design. It does not mean the same page structure, dark theme, canvas composition, moving dots, sliders, readouts, or physics-style simulation every time.

## Supporting Skill

Because this skill creates a frontend artifact, also apply `.agents/skills/frontend-design/SKILL.md` as a supporting design-quality guideline.

Use `frontend-design` for:
- aesthetic direction,
- typography,
- colour,
- layout,
- motion,
- responsiveness,
- polish.

Do not let `frontend-design` override this skill's requirements for factual accuracy, topic-fit, educational clarity, code rendering, no image generation, and explanation below the visual.

## Trigger

Use this skill when the user says or clearly means:
- "Show me ..."
- "Visualize ..."
- "Explain visually ..."
- "Make an interactive infographic about ..."
- "Create an interactive explainer for ..."

Do not use this skill when the user asks for AI image generation or only wants a normal text explanation.

## Required Output

Generate the interactive visual first, then place explanation below it.

Preferred output:
1. A single rendered React component.
2. A topic-specific visual as the dominant first element.
3. Controls only when they clarify the concept.
4. Readouts, labels, legends, or annotations connected to the controls.
5. Concise educational explanation below the visual.

Do not use AI image generation. Do not merely describe the infographic unless rendering is impossible.

## Topic-Fit Contract

Before coding, decide the actual visual contract for the topic. The final artifact must visibly satisfy it.

Define internally:
- Topic-native objects: the real things, actors, structures, evidence, stages, forces, regions, entities, or examples that belong to the concept.
- Topic-native variables: the real quantities, states, choices, phases, weights, categories, or conditions that change understanding.
- Topic-native relationships: the causal, spatial, temporal, mathematical, anatomical, social, or logical relationships that must be visible.
- Learner misconception: the wrong mental model the visual should correct.
- Visual proof: at least three visible details that would be wrong or meaningless if copied into an unrelated topic.

If these cannot be defined, redesign before implementation.

The visual must answer:
- What actual thing am I looking at?
- What changes?
- Why does that change matter for this topic?

## Visual Model Selection

Choose a visual model from the topic, not from habit.

| Topic type | Better visual models | Better controls |
|---|---|---|
| Mechanism or process | causal chain, staged animation, state transition, system cutaway | stepper, speed, reveal labels |
| Physical law or engineering | direct simulation, force diagram, graph plus object, specimen view | real parameter sliders, material selector, overlay toggle |
| Biology or anatomy | labelled cross-section, pathway, layer stack, zoomed tissue/organ region | layer toggles, stage selector, pathology toggle |
| Chemistry | particle model, reaction pathway, energy diagram, concentration field | concentration, temperature, phase, catalyst toggle |
| Mathematics | graph, geometric construction, transformation, numeric-to-visual mapping | parameter sliders, formula toggle, compare cases |
| Statistics | distribution, sampling view, confidence region, error/bias comparison | sample size, mean, variance, group selector |
| History or timeline | timeline, cause-effect map, actors and pressures, branching path | era selector, theme highlight, sequence scrubber |
| Comparison | aligned scales, matrix, before/after, tradeoff map | category selector, sort mode, highlight differences |
| System or network | nodes, flows, feedback loops, bottlenecks, failure modes | isolate subsystem, toggle flows, stress condition |
| Scale or spectrum | logarithmic scale, nested zoom, gradient with markers | zoom, marker, scale mode |
| Abstract or social concept | evidence map, lens/filter, scenario comparison, decision tree, perspective map | evidence mix, perspective toggle, bias weight, mitigation stepper |
| Definition or language concept | semantic map, examples/non-examples, boundary cases, contrast pairs | reveal layers, compare cases, ambiguity slider |

Examples of topic-fit:
- Electricity: circuit path, battery potential difference, load, current/charge flow, field direction, resistance, power.
- Light: wave/ray optics, wavelength, photon energy, spectrum marker, reflection/refraction boundary, medium.
- Tensile strength: specimen under load, stress-strain curve, strain, material, elastic/yield/UTS/fracture regions.
- Bias: evidence points, prior-belief weighting, ignored counter-evidence, shifted judgement, checking/mitigation loop.
- Democracy: voters, representatives, institutions, rules, accountability loops, information flow, failure points.
- Inflation: basket of goods, price index over time, purchasing power, wage lag, demand/supply pressure, policy levers.
- Photosynthesis: chloroplast structure, light reactions, carbon fixation, inputs/outputs, energy carriers.

## Layout Rules

Use one coherent infographic page. The page structure must be chosen for the topic.

Allowed layout archetypes:
- single-stage simulation,
- split comparison,
- graph plus object view,
- timeline track,
- layered cross-section,
- network map,
- matrix or spectrum,
- guided stepper,
- zoom lens or nested scale view,
- scenario comparison,
- decision tree.

Do not default to:
- one large rectangular canvas,
- horizontal controls below it,
- three readout boxes,
- dark technical grid,
- moving dots,
- generic arrows,
- the same explanatory paragraph structure.

Use those only when they genuinely fit the topic.

## Design Direction

Use `frontend-design` to choose a deliberate aesthetic direction for the specific subject.

The design may be dark, light, clinical, editorial, industrial, academic, playful, brutalist, refined, dense, sparse, or another suitable direction. The choice must support the concept and audience.

Avoid:
- generic AI aesthetics,
- purple gradients on white by default,
- Inter/system typography by default,
- card dashboards unless the task needs cards,
- decorative effects unrelated to the concept,
- designs that would work unchanged for another topic.

Use:
- topic-specific palette and accent logic,
- typography that fits the subject,
- semantic colour,
- labels placed near what they explain,
- motion only where it teaches,
- responsive layout with no overlapping text or controls.

## Interactivity Rules

Add controls only when they improve understanding.

Every control must update at least two of:
- the main visual,
- a label,
- a readout,
- a highlighted region,
- an explanatory sentence,
- animation state.

Controls must be concept-specific:
- voltage for a circuit,
- strain for tensile strength,
- wavelength for light,
- phase for mitosis,
- sample size for statistics,
- evidence weighting for bias,
- era/actor focus for history.

Do not use a generic "strength" slider unless strength is the actual concept variable.

## Implementation Rules

Default to:
- a single React component,
- Tailwind CSS utilities,
- Canvas 2D for dynamic diagrams when appropriate,
- React state for controls,
- `useMemo`, `useRef`, and `useEffect` where useful,
- `requestAnimationFrame` only for meaningful animation.

Canvas is preferred for simulations and custom diagrams, but HTML/CSS layout, SVG, or mixed rendering is acceptable when it is a better technical fit. Do not force Canvas if the concept is better represented as a timeline, matrix, semantic map, or structured layout.

The component must:
- be self-contained,
- default export one component,
- avoid unnecessary dependencies,
- use clear constants for the concept model,
- include accessible labels for controls,
- be responsive,
- avoid dead controls.

## Anti-Template Gate

Reject and redesign before final output if:
- the title is the only topic-specific part,
- fewer than three visible elements are topic-native,
- the same layout would work for the previous unrelated topic,
- an abstract/social/history topic is forced into a physics simulation,
- a physical/biological mechanism is reduced to a vague metaphor when direct representation is possible,
- labels describe relationships that are not visible,
- the result feels like a dashboard about the topic instead of an infographic that reveals the topic.

## Knowledge Rules

Verify or source facts when:
- the topic is medical, legal, financial, safety-related, or high-stakes,
- the user asks for current information,
- numerical constants, ranges, standards, or classifications matter,
- the topic is niche or unfamiliar.

Never fabricate statistics, thresholds, citations, mechanisms, anatomical details, or clinical claims.

Mark simplified educational models as simplified when needed.

## Explanation Below the Visual

The explanation should be concise but substantial.

Recommended structure:
1. Big-picture sentence.
2. Three to five short paragraphs, each starting with a bold key concept.
3. Tie explanation to what the visual shows and what controls change.

Use correct terminology and units wherever numeric values appear.

## Workflow

1. Parse topic, learning goal, scope, domain, and whether controls help.
2. Load `frontend-design` as a supporting design-quality layer.
3. Define the Topic-Fit Contract.
4. Choose visual model, layout archetype, aesthetic direction, and control model.
5. Build the artifact with topic-native geometry, labels, interactions, and responsive polish.
6. Write the explanation below the visual.
7. Apply the Anti-Template Gate before finalizing.

## Success Tests

A successful output passes these tests:
1. If the title were removed, the visual still suggests the topic.
2. If the controls were removed, the visual still teaches something.
3. If the explanation were removed, the main structure is still understandable.
4. At least three visible elements would be wrong in an unrelated topic.
5. The design feels deliberately made for this prompt.
6. The visual model changes when the topic changes.
