# Simulation Design

## Purpose

Design simulations and interactive models that are educational, truthful, and testable.

## Workflow

1. Define the learning goal
   - What should the user understand after interacting with it?
   - What misconception should the simulation correct?

2. Define the model
   - State variables.
   - Inputs and controls.
   - Outputs and readouts.
   - Units and scales.
   - Simplifying assumptions.

3. Choose representation
   - Direct physical/anatomical/system representation when possible.
   - Graph plus object view for measurable concepts.
   - Timeline or stepper for sequences.
   - Network or feedback loop for systems.
   - Distribution view for statistical concepts.

4. Define update rules
   - Equations or qualitative transitions.
   - Time step and stability considerations.
   - Bounds and extreme values.

5. Design interactions
   - Each control should change the model visibly.
   - Continuous animation should include pause/resume.
   - Include reset or default state when helpful.

6. Verify
   - Check limiting cases.
   - Check units.
   - Check qualitative behavior against expected theory.
   - Confirm controls affect readouts and visuals consistently.
   - Confirm the simulation does not imply unsupported precision.

7. Explain
   - Describe what is simplified.
   - Explain how to interpret controls and readouts.
   - State what should not be inferred from the model.

## Quality criteria

A good simulation:
- teaches cause and effect,
- makes invisible relationships visible,
- remains stable at extreme settings,
- has meaningful controls,
- has readable labels,
- is honest about simplification.

## Failure modes

Avoid:
- decorative animation without learning value,
- fake numbers,
- controls that only change labels,
- unstable or unbounded model behavior,
- presenting a qualitative model as quantitative prediction.
