# Plume Plat Compose Mesh Walkthrough

I use this file as a small checklist before changing the Java implementation.

| Case | Focus | Score | Lane |
| --- | --- | ---: | --- |
| baseline | rollout width | 223 | ship |
| stress | quota pressure | 141 | ship |
| edge | route drift | 167 | ship |
| recovery | secret scope | 176 | ship |
| stale | rollout width | 185 | ship |

Start with `baseline` and `stress`. They create the widest contrast in this repository's fixture set, which makes them better review anchors than the middle cases.

The next useful expansion would be a malformed fixture around quota pressure and secret scope.
