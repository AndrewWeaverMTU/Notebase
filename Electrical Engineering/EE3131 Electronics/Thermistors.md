- A resistor with a resistance that is **strongly** dependent on temperature
	- (all resistors are temp dependent, thermistors are REALLY temp dependent)
- 

### Simple Linear Model
$$\Delta R = \alpha\Delta T$$
- Only accurate for small $\Delta T$
- $\Delta R$ - Change in resistance
- $\Delta T$ - Change in temperature
- $\alpha$ - Some temperature coefficient
	- $\alpha > 0$ - “Positive Temp Coefficient” (PTC) Thermistor, used in circuit protection
	- $\alpha < 0$ - “Negative Temp Coefficient” (NTC) Thermistor, used in temperature measurements (sensor applications)

### Diagram

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2026.1.9 - 11.24am.drawing",
	"width": 100,
	"aspectRatio": 1
}
```

### PTC Circuit Protection Example
```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2026.1.9 - 11.25am.drawing",
	"width": 300,
	"aspectRatio": 1
}
```
- As P increases, temperature increases. As temperature increases, resistance increases. If the load draws too much current, the PTC blocks it.

### Steinhart-Hart Equation
- Better model, used for sensing purposes
$$T = \frac{1}{a + b\ln(R) + c\ln^3(R)}$$
- R - Resistance
- T - Abs. Temperature in Kelvin
- a, b, and c are parameters tuned for a specific device
- Can be experimentally determined by measuring it across a bunch of known temperatures. Need at least 3 data points, then solve/fit a line.