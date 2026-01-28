## Offset Voltage
- For a real [[Operational Amplifiers|Op Amp]] with both inputs at 0V, the output likely will not be zero.
- If the inputs are even slightly off ($1\mu V$), it’s output won’t be zero

#### Correcting
- Not all op amp designed are easily corrected
- Many op-amps provide a set of “offset-null terminals that can be used to correct the input voltage offset.
	- Potentiometer is used between the adjustment terminals with the third terminal connected to $V_{neg}$

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2026.1.28 - 11.18am.drawing",
	"width": 300,
	"aspectRatio": 1
}
```
## Input Bias & Offset Current
- Real op-amps do draw a minuscule amount of current at the input terminals, particularly for [[Bipolar Junction Transistor]]-based op-amps
- in the nanoampere range for BJTs
- If there is an offset, $I_{io} = I_+ - I_-$

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2026.1.28 - 11.26am.drawing",
	"width": 529,
	"aspectRatio": 0.8324154209284028
}
```
#### Correcting

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2026.1.28 - 11.32am.drawing",
	"width": 500,
	"aspectRatio": 1
}
```
