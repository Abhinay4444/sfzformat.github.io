# off_mode

Region off mode. This opcode will determinate how a region is turned off by an
[off_by](/opcodes/sfz_1/off_by) opcode. There are two choices:

- fast (default): The voice will be turned off immediately.
  Release settings will not have any effect.
- normal: The region will be set into release stage. All envelope generators
  will enter in release stage, and region will expire when the amplifier
  envelope generator expired.

ARIA also adds off_mode=time which can be used to specify a time independent of
the sample release time using [off_time](/extensions/aria/opcodes/off_time),
and also [off_shape](/extensions/aria/opcodes/off_shape) and [off_curve](/extensions/aria/opcodes/off_curve)
to control the curve of the fadeout.

Examples:

```
off_mode=fast

off_mode=normal
```

Note that the default is fast, and not normal, which means that
"normal isn't normal", and if normal is needed, it will need to be set explicitly.
Normal is useful for legato instruments where a fading in the previous samples
while the new one fades in is desirable, and can also be useful for making hi-hat
muting behavior sound a little more natural. With longer release times,
off_mode=normal is also a way to manage buildup in instruments which have a very
long sustain and can have the sound of several notes build up - for example,
hammered dulcimers or ride cymbals.