# Ion Trade Fills Gate Walkthrough

The fixture is intentionally compact, so the review starts with the cases that pull farthest apart.

| Case | Focus | Score | Lane |
| --- | --- | ---: | --- |
| baseline | spread pressure | 156 | ship |
| stress | fill risk | 132 | watch |
| edge | portfolio drift | 133 | watch |
| recovery | quote width | 172 | ship |
| stale | spread pressure | 179 | ship |

Start with `stale` and `stress`. They create the widest contrast in this repository's fixture set, which makes them better review anchors than the middle cases.

`stale` is the optimistic case; use it to make sure the scoring path still rewards strong signal.
