## Ohm’s Law
- V = I R 

## Joule’s Heating 
- Power consumption through a resistor can be defined as P = I^2 R
- Usually dissipated as heat
- Derived from P = IV and V = IR to get P = I^2 R

## Sign Conventions

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2026.1.5 - 11.33am.drawing",
	"width": 500,
	"aspectRatio": 1
}
```

- **Passive Sign Convention** - Voltage drops are positive
- When you go from a negative to a positive, your voltage (and power) INCREASE



## Superposition
- With dependent sources, we can analyze a circuit under each source, then sum up the voltages/currents to get the whole circuit.


```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2026.1.7 - 11.06am.drawing",
	"width": 524,
	"aspectRatio": 0.7867867867867868
}
```

## Thevenin Equivalent Circuits
- Any **linear circuit** can be rewritten as a voltage source in series with a resistor from the perspective of the load (wherever we’re measuring from)
To find a thevenin equivalent:
1. find the thevenin Voltage - the open circuit voltage across the terminals
2. Find the thevenin resistance - The equivalent resistance (or impedance) seen at the terminals with all independed sources considered inactive (voltage -> short, current -> open)

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2026.1.7 - 11.13am.drawing",
	"width": 482,
	"aspectRatio": 0.4762845849802372
}
```


```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2026.1.7 - 11.25am.drawing",
	"width": 448,
	"aspectRatio": 0.5678073510773131
}
```

## Voltage-Current Relationships
- Changes for different elements
- current is usually somehow related to voltages
- i = f(v)
- Used when calculating the Thevenin equivalent

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2026.1.5 - 11.50am.drawing",
	"width": 500,
	"aspectRatio": 1
}
```
