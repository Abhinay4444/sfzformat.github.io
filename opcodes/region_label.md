---
lang: en
title: region_label
---
An ARIA extension which sets what is displayed in the default info tab of Sforzando. Useful for debugging.
It can be set anywhere, not just under the <[region](/headers/region)> header. If not set, the info tab
will display the file path of the most recently played sample.

See also [global_label](global_label), [master_label](master_label) and [group_label](group_label).

##### Examples

```
group_label=C3 staccato piano RR4
group_label=Snare rimshot 28
```

| Type    | Default | Range           |
| ---     | ---     | ---             |
| text    | null    | N/A             |