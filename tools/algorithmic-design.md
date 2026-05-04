# Algorithmic Design

## Purpose

Improve algorithm choice, implementation planning, and correctness for programming, simulations, data processing, optimization, and reasoning tasks.

## Workflow

1. Define the contract
   - Inputs.
   - Outputs.
   - Constraints.
   - Required exactness or approximation.
   - Performance targets.

2. Identify edge cases
   - Empty input.
   - Single item.
   - Duplicates.
   - Missing data.
   - Invalid input.
   - Very large input.
   - Numerical extremes.

3. Choose approach
   - Brute force baseline.
   - Better data structure or algorithm.
   - Tradeoffs in time, space, readability, and maintainability.

4. Prove or justify correctness
   - Invariant.
   - Recurrence.
   - Greedy choice reasoning.
   - Exhaustiveness.
   - Counterexample search.

5. Analyze complexity
   - Time complexity.
   - Space complexity.
   - Practical bottlenecks.

6. Implement
   - Keep code clear.
   - Preserve existing project style.
   - Use tests for edge cases.

7. Verify
   - Compare against brute force for small cases when feasible.
   - Use property-style checks when useful.
   - Include regression tests for discovered bugs.

## Tool ideas

A future helper script could provide:
- brute-force comparison harnesses,
- randomized small-case generators,
- invariant checks,
- performance microbenchmarks,
- graph/search templates,
- numerical stability checks.
