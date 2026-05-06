# plume-plat-compose-mesh

`plume-plat-compose-mesh` explores platform engineering with a small Java codebase and local fixtures. The technical goal is to package a Java local lab for compose analysis with node-edge fixtures, cycle and reachability reports, and documented operating limits.

## Why I Keep It Small

The project exists to keep a narrow engineering decision visible and testable. For this repo, that decision is how rollout width and route drift should influence a review result.

## Plume Plat Compose Mesh Review Notes

For a quick review, compare `rollout width` with `quota pressure` before reading the middle cases.

## Included Behavior

- `fixtures/domain_review.csv` adds cases for rollout width and quota pressure.
- `metadata/domain-review.json` records the same cases in structured form.
- `config/review-profile.json` captures the read order and the two review questions.
- `examples/plume-plat-compose-walkthrough.md` walks through the case spread.
- The Java code includes a review path for `rollout width` and `quota pressure`.
- `docs/field-notes.md` explains the strongest and weakest cases.

## Internal Model

The repository has two validation layers: the original compact policy fixture and the domain review fixture. They are separate so one can change without hiding failures in the other.

The Java implementation avoids hidden state so fixture changes are easy to reason about.

## Try It Locally

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -File scripts/verify.ps1
```

## Validation

The verifier is intentionally local. It should fail if the fixture score math, lane assignment, or language-specific test drifts.

## Scope

No external service is required. A deeper version would add more negative cases and a clearer boundary around invalid input.
