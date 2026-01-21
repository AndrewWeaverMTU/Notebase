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

### Minimizing SOP Equations
- We could just factor, but there is an easier systematical way called Karnaugh maps
- K-maps show the variables and their pairings. For example,

| A   | B   | X   |
| --- | --- | --- |
| 0   | 0   | F0  |
| 0   | 1   | F1  |
| 1   | 0   | F2  |
| 1   | 1   | F3  |
Becomes

| B      A | 0   | 1   |
| -------- | --- | --- |
| 0        | F0  | F2  |
| 1        | F1  | F3  |
- Our goal is to find [[Implicants]], particularly [[Implicants#^d589c2|EPIs]]. Our full procedure is as follows:
	1) Select an un-circled 1. Circle it. Can it get bigger?
	2) Keep getting bigger until it is a prime implicant
	3) Are all 1's circled? If not, go back to step 1.
	4) Underline all of the distinguished 1 cells.
	5) Erase the smallest prime implicants that are not essential (don't contain d-1 cells)
	6) Continue until you only have EPIs
- **the edges of K-maps are like little portals. If 1s are adjacent on both sides, you can make one big implicant. The same goes for the corners**
- Once you've got the implicants, generate an exxpression using the values that stay the same within each implicant, then or them together.
#### Kmap Edge Example

| CD \| AB | 00  | 01  | 11  | 10  |
| -------- | --- | --- | --- | --- |
| 00       |     |     |     |     |
| 01       | 1   |     |     | 1   |
| 11       | 1   |     |     | 1   |
| 00       |     |     |     |     |
- The two 1-implicants here make one big Prime implicant by carrying over the edge.

| CD \| AB | 00  | 01  | 11  | 10  |
| -------- | --- | --- | --- | --- |
| 00       | 1   |     |     | 1   |
| 01       |     |     |     |     |
| 11       |     |     |     |     |
| 00       | 1   |     |     | 1   |
- The four corners make an implicant

### Kmap Filling Diagrams

| a   | b   | c   | x   |
| --- | --- | --- | --- |
| 0   | 0   | 0   | f0  |
| 0   | 0   | 1   | f1  |
| 0   | 1   | 0   | f2  |
| 0   | 1   | 1   | f3  |
| 1   | 0   | 0   | f4  |
| 1   | 0   | 1   | f5  |
| 1   | 1   | 0   | f6  |
| 1   | 1   | 1   | f7  |
Becomes

| C  \|    AB | 00  | 01  | 11  | 10  |
| ----------- | --- | --- | --- | --- |
| 0           | F0  | F2  | F6  | F4  |
| 1           | f1  | f3  | f5  | f7  |
- **AB's order is VERY important. 00 01 11 10 (breakcode), not 00 01 10 11 (binary)**

#### 2-input example
Find the simplest mathematical representation of $F = \sum_{AB}(1,3)$

1) Generate truth table

| A   | B   | X   |
| --- | --- | --- |
| 0   | 0   | 0   |
| 0   | 1   | 1   |
| 1   | 0   | 0   |
| 1   | 1   | 1   |
2) Generate K-map

| B        A | 0   | 1   |
| ---------- | --- | --- |
| 0          | 0   | 0   |
| 1          | 1   | 1   |
3) Create representation
$X = B$

#### 3-input example

| a   | b   | c   | x   |
| --- | --- | --- | --- |
| 0   | 0   | 0   | 0   |
| 0   | 0   | 1   | 1   |
| 0   | 1   | 0   | 0   |
| 0   | 1   | 1   | 1   |
| 1   | 0   | 0   | 1   |
| 1   | 0   | 1   | 1   |
| 1   | 1   | 0   | 1   |
| 1   | 1   | 1   | 1   |
becomes

| C \|   AB | 00  | 01  | 11  | 10  |
| --------- | --- | --- | --- | --- |
| 0         | 0   | 0   | 1   | 1   |
| 1         | 1   | 1   | 1   | 1   |
|           |     |     |     |     |
becomes
$X = C + A$, as 1 appears when A or C is true.

### 5-Variable Karnaugh Map
- Uses two maps that are basically stacked on top of each other
- Implicants become 3D