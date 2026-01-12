- Gates can be linked to others to create more complex logic
- Constructing intermittent/placeholder vars can sometimes be helpful 

## Precedence order
1. Parentheses
2. Inversion
3. And
4. Or
### Example

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2026.1.7 - 13.39pm.drawing",
	"width": 300,
	"aspectRatio": 1
}
```

#### Truth Table for Example

| A   | B   | C   | A’  | C’  | M   | T   | X   |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 0   | 0   | 0   | 1   | 1   | 0   | 0   | 0   |
| 0   | 0   | 1   | 1   | 0   | 0   | 0   | 0   |
| 0   | 1   | 0   | 1   | 1   | 1   | 1   | 1   |
| 0   | 1   | 1   | 1   | 0   | 1   | 0   | 1   |
| 1   | 0   | 0   | 0   | 1   | 0   | 0   | 0   |
| 1   | 0   | 1   | 0   | 0   | 0   | 1   | 1   |
| 1   | 1   | 1   | 0   | 0   | 0   | 0   | 0   |
### Example - Eqn To Logic Diagram

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2026.1.7 - 13.47pm.drawing",
	"width": 500,
	"aspectRatio": 1
}
```
