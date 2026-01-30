- [[Operational Amplifiers|Op-Amp]] gain is dependent on frequency
- $A_o$ is assumed to be at DC
- For AC, $\huge A(j\omega) = \frac{A_0}{1 + j \frac{\omega}{\omega_p}}$
	- $\omega_p$ -> the point at which the gain begins to decrease, kind of like the cutoff frequency.
```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2026.1.30 - 11.06am.drawing",
	"width": 360,
	"aspectRatio": 2.4
}
```
## Gain-bandwidth Product

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2026.1.30 - 11.08am.drawing",
	"width": 300,
	"aspectRatio": 1.8841870824053453
}
```
$$\huge A_0 \times B_0 = A_{fb} \times B_{fw}$$
- The gain times the bandwidth is always the same, regardless of frequency

## Slew Rate Limitation
- There is a specific maximum rate of change possible at the output of a real op-amp. This maximum is called the **slew rate** (sR) of the op amp
- in general, the sR is $\huge \frac{1V}{\mu S}$
- This determines the maximum operating frequency. 
$$\huge \frac{dV_{out}}{dt} \biggr\rvert_{at \space \omega\\t = 0} = \frac{d}{dt}\left[V_0\sin(\omega\\t)\right] = \omega V_0 = 2\pi f \cdot V_0$$
- If sR = $\huge\frac{1V}{\mu\\s}$, $f = 16kHz$ 

## Output Current Limitation
- The output current of an op amp is limited, usually in the $\pm25mA$  range
- If an attempt is made to exceed the limit, the internal circuitry will reduce the internal gain to limit the current.