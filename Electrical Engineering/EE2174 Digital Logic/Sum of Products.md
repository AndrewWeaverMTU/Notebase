- A procedure for generating a [[Boolean Algebra]] equation from a truth table

### Procedure
- For any 1 outputs, [[And Gate|AND]] the things in that row, [[NOT Gate|NOT]] any zeroes, then [[OR Gate|OR]] the generated terms.
- Ignore any 0 outputs.

### Example

| A   | B   | Z   |
| --- | --- | --- |
| 0   | 0   | 0   |
| 0   | 1   | 1   |
| 1   | 0   | 1   |
| 0   | 0   | 0   |

```handwritten-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Writing/2026.1.12 - 13.30pm.writing"
}
```

## Shorthand
- We can also use a shorthand notation where we write things as a sum of the # rows that have 1 minterms (products)
- Each row’s inputs correspond to the binary number represented in the shorthand.


| Binary # | A   | B   | Z   |
| -------- | --- | --- | --- |
| 0        | 0   | 0   | 0   |
| 1        | 0   | 1   | 1   |
| 2        | 1   | 0   | 1   |
| 3        | 1   | 1   | 0   |
Becomes: $$\sum_{(A,B,C)}(1,2)$$

Example:


```handwritten-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Writing/2026.1.12 - 13.34pm.writing"
}
```
