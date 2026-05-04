# Quality Levels

Quality levels control how much verification and depth to apply.

## Default

Use `L1-reliable-default.md` unless a different level is requested or required.

## Levels

| Level | Name | Use when |
|---|---|---|
| L0 | Fast Direct | The answer is simple, stable, and low risk |
| L1 | Reliable Default | Most normal prompts |
| L2 | Verified | Citations, current facts, exact numbers, or uncertainty matter |
| L3 | High Stakes | Medical, legal, financial, safety, ethics, academic-critical |
| L4 | Production Artifact | Code/files/artifacts must be generated, validated, and linked |

Escalate at least to L2 for file research, OCR extraction, complex calculations, simulations, and contested world topics. Escalate to L4 when a tangible artifact or code change must be created and checked.
