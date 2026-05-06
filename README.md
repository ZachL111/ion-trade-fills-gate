# ion-trade-fills-gate

`ion-trade-fills-gate` explores trading systems with a small Zig codebase and local fixtures. The technical goal is to design a Zig verification harness for fills systems, covering security rule linting, safe and unsafe fixtures, and failure-oriented tests.

## Purpose

This is intentionally local and self-contained so it can be inspected without credentials, services, or seeded history.

## Ion Trade Fills Gate Review Notes

Start with `spread pressure` and `fill risk`. Those cases create the widest score spread in this repo, so they are the best quick check when the model changes.

## What Is Covered

- `fixtures/domain_review.csv` adds cases for spread pressure and fill risk.
- `metadata/domain-review.json` records the same cases in structured form.
- `config/review-profile.json` captures the read order and the two review questions.
- `examples/ion-trade-fills-walkthrough.md` walks through the case spread.
- The Zig code includes a review path for `spread pressure` and `fill risk`.
- `docs/field-notes.md` explains the strongest and weakest cases.

## Implementation Notes

The implementation keeps the scoring rule plain: reward signal and confidence, preserve slack, penalize drag, then classify the result into a review lane.

The added Zig path is deliberately direct, with fixtures doing most of the explaining.

## Command

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -File scripts/verify.ps1
```

## Audit Path

The check exercises the source code and the review fixture. `stale` is the high score at 179; `stress` is the low score at 132.

## Limits

The fixture set is small enough to audit by hand. The next useful expansion is malformed input coverage, not extra surface area.
