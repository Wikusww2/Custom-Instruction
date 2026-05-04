# Simulations and Modeling

## Goal

Create simulations and models that teach the real mechanism without pretending to be more accurate than they are.

Use this module for interactive simulations, visual explainers, computational models, physics/biology/economics/clinical models, algorithms with dynamic behavior, and "show how it works" requests.

## Model clarity

Before building or explaining a simulation:
- define what the model represents,
- define what it leaves out,
- list state variables,
- list inputs and controls,
- list outputs/readouts,
- identify units and scales,
- state whether the model is qualitative, semi-quantitative, or quantitative.

## Simulation design

Use `tools/simulation-design.md` for non-trivial simulations.

Good simulations:
- expose meaningful parameters,
- show cause and effect visibly,
- include labels tied to the model,
- keep animation purposeful,
- include pause/reset or step controls when continuous motion could distract,
- handle extreme values without breaking,
- avoid fake precision.

## Verification

Check:
- limiting cases,
- conservation or balance laws where relevant,
- units,
- expected qualitative behavior,
- numerical stability,
- whether controls actually affect the model.

## Explanation

Explain:
- what the viewer is seeing,
- which assumptions are simplified,
- how controls affect the system,
- where the model differs from the real world,
- what the learner should conclude.
