---
layout: sfz/opcode
lang: en
title: tune
---
Range in the SFZ1 spec is ±1 semitone, from -100 to 100, though at least in ARIA,
it seems a broader range is supported, at least -2400 to 2400 cents.

##### Examples

```
tune=33

tune=-30

tune=94
```

Uses include correcting the intonation of naturally off-pitch samples, and
detuning unison voices.
