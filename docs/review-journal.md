# Review Journal

This journal records the domain cases that matter before widening the public API.

The local checks classify each case as `ship`, `watch`, or `hold`. That gives the project a small review vocabulary that matches its trading systems focus without claiming live deployment or external usage.

## Cases

- `baseline`: `spread pressure`, score 156, lane `ship`
- `stress`: `fill risk`, score 132, lane `watch`
- `edge`: `portfolio drift`, score 133, lane `watch`
- `recovery`: `quote width`, score 172, lane `ship`
- `stale`: `spread pressure`, score 179, lane `ship`

## Note

A future change should add new cases before it changes the scoring rule.
