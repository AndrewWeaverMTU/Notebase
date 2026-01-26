- Linear devices
- Made up of many (20-30) transistors integrated on a chip (IC)
- Generally have two input terminals and one output, plus two supply terminals.

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2026.1.12 - 11.00am.drawing",
	"width": 200,
	"aspectRatio": 1.3298429319371727
}
```
## Ouptut of an Op-Amp
$$v_\text{out} = A_0 \cdot(v_+ - v_-)$$
- $A_0$ is called the *open loop gain*. In an ideal case, it is $\infty$. In reality, it’s usually between $1\times10^5$ and $1\times10^6$
- The output is limited by the supply voltages. $V_\text{NEG} \le v_\text{out} \le V_\text{POS}$
```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2026.1.12 - 11.30am.drawing",
	"width": 300,
	"aspectRatio": 1
}
```


## Ideal Op-Amp Approximations
- Assume the following:
	- Infinite input resistance. ($i_+ = i_- = 0$)
	- Zero output resistance. 
	- Infinite open loop/internal gain ($A_0 \to \infty$)
	- Output is limited by negative and positive supply voltages. ($V_\text{NEG} \le v_{out} \le V_\text{POS}$)
		- if $v_+ - v_- \to +$, then $v_{out} = V_\text{POS}$
		- if $v_+ - v_- \to -$, then $v_{out} = V_\text{NEG}$
		- if $v_+ - v_- = 0$, then $V_\text{NEG}< v_{out} < V_\text{POS}$ (called a virtual short)

### Virtual Shorts
- For ideal op-amp analysis with negative feedback, the two input terminals should have the same voltage, creating a “virtual short”
- By assuming a virtual short, we can greatly simplify op-amp analysis (see inverting config example 2 [[#^6e1bb5|here]])
### Input Resistance
- $R_{in} = \frac{v_{in}}{i_{in}}$
# Op-Amp Configurations
## Inverting Configuration

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2026.1.12 - 11.39am.drawing",
	"width": 430,
	"aspectRatio": 2.349726775956284
}
```
- Feedback circuit - output is determined by the inputs, but the output also alters the input until an equilibrium is reached.
- For an inverting configuration, the closed loop gain is $\frac{v_{out}}{v_{in}} = -\frac{R_2}{R_1}$ 
	- If $R_2 = R_1$, then $v_{out} = -v_{in}$, thus inverting the signal. 
#### Inverting Config Example

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2026.1.14 - 11.10am.drawing",
	"width": 504,
	"aspectRatio": 0.782608695652174
}
```
#### Inverting Config With Virtual Short

^6e1bb5

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2026.1.14 - 11.23am.drawing",
	"width": 500,
	"aspectRatio": 1
}
```
### Summation Amplifier
- Used to mix signals into a single track
	- Could be used in primitive audio processing
	- 
```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2026.1.14 - 11.34am.drawing",
	"width": 450,
	"aspectRatio": 2.830188679245283
}
```
#### Summation Ex1

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2026.1.14 - 11.37am.drawing",
	"width": 404,
	"aspectRatio": 0.8782608695652174
}
```
## Noninverting Configuration

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2026.1.16 - 11.00am.drawing",
	"width": 250,
	"aspectRatio": 1
}
```
- Infinite Input Resistance (0 input current, $\lim_{i\to\\0} \frac{v}{i} = \infty = R_{in}$)
### $V_{out}$ equation
$$v_{out} = \left( 1 + \frac{R_2}{R_1}\right)\cdot v_{in}$$
### Solving Example

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2026.1.16 - 11.02am.drawing",
	"width": 400,
	"aspectRatio": 1
}
```

## Voltage Follower (Buffer Follower) Configuration

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2026.1.16 - 11.15am.drawing",
	"width": 250,
	"aspectRatio": 2.208588957055215
}
```
- $v_{out} = v_{in}$, $R_{in} = \lim_{i\to\\0} \frac{v}{i}= \infty$
- Used to maintain voltage but block current, thereby ignoring resistors afterwards
### Example Setup

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2026.1.16 - 11.19am.drawing",
	"width": 300,
	"aspectRatio": 0.5432372505543237
}
```

## Difference Amplifier

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2026.1.16 - 11.35am.drawing",
	"width": 300,
	"aspectRatio": 1
}
```
- Very rarely used, too many resistors to deal with & non-infinite input resistance.´
$$v_{out} = \frac{R_2}{R_1} \cdot (v_2 - v_1)$$
- only if R2 = R4 and R1 = R3


### Differential & Common Mode Input
- Differential - $V_{in} = v_+- v_-$
- Common $V_{in} = \frac{1}{2}(v_- + v_+)$

### Solving

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2026.1.16 - 11.36am.drawing",
	"width": 504,
	"aspectRatio": 0.7567567567567568
}
```

### Difference Amp w/ Common Mode Input

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2026.1.26 - 11.26am.drawing",
	"width": 439,
	"aspectRatio": 0.3152603231597846
}
```

## Omp-Amp Integrator Configuration (Inverting Integrator)

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2026.1.21 - 11.26am.drawing",
	"width": 300,
	"aspectRatio": 1
}
```

### Solving

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2026.1.21 - 11.28am.drawing",
	"width": 500,
	"aspectRatio": 1
}
```

## Op-Amp Differentiator Configuration
- Inverting differentiator

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2026.1.21 - 11.38am.drawing",
	"width": 300,
	"aspectRatio": 1
}
```
### Solving - Differential Config

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2026.1.21 - 11.39am.drawing",
	"width": 500,
	"aspectRatio": 1
}
```
## Inverting Schmitt Trigger Configuration                
```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2026.1.21 - 11.47am.drawing",
	"width": 300,
	"aspectRatio": 1
}
```
- **Positive** feedback circuit.
- Acts as a comparator
- Vout will equal Vpos or Vneg
- If $V_{out} = V_{pos}$

## Implementation Amplifier Configuration


# Internal Operation
 3 Major Steps:
 1. Differential Amplifier - 2 inputs - Inverting (v-) and non-inverting (v+) terminals
	- 2 inputs -> 1 output
	- Output is proportional to the difference of the two inputs
	- $\text{Output} = a_1 \cdot (v_+ - v_-)$
 2. High Gain Stage
	 - Adding gain to the output from the differential amplifier
	 - $\text{Output} = a_1 \cdot a_2 \cdot (v_+ - v_-)$
3. Output Stage
	- Single output termial
	- Output current is provided by this stage. The gain is generally 1 in this stage.

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2026.1.12 - 11.07am.drawing",
	"width": 500,
	"aspectRatio": 1.7751937984496124
}
```
- Minimum of five terminals on the op-amp: $V_\text{pos} \text { \& } V_{neg}$ (Supply Voltages), $v_+ \space\& \space v_-$(input voltages), and the output.