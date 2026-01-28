- How we mathematically manipulate boolean eqns

### Single Variable Theorems


| T1     | $X + 0 = X$  | X or’d with 0 is still X      | Identities    |
| ------ | ------------ | ----------------------------- | ------------- |
| **T2** | $X + 1 = 1$  | X or’d with 1 is always 1     | Null elements |
| **T3** | $X + X = X$  | X or’d with X is still X      | Idempotency   |
| **T4** | $(X’)’ = X$  | X not not is X                | Involution    |
| **T5** | $X + X’ = 1$ | X or’d with X’ is always true | Complements   |
### Multivar Theorems

| T6  | $X + Y = Y + X$                           | You can switch the order of inputs for an or                         | Commutativity  |
| --- | ----------------------------------------- | -------------------------------------------------------------------- | -------------- |
| T7  | $(X + Y) + Z = X + (Y + Z)$               | It doesn’t matter in what order you do or gates if it’s all or gates | Associativity  |
| T8  | $X \cdot Y + X \cdot Z = X \cdot (Y + Z)$ | Factoring Works!                                                     | Distributivity |
| T9  | $X + X \cdot Y = X$                       | Factoring works! See T2                                              | Covering       |
| T10 | $X \cdot Y + X \cdot Y’ = X$              | Factoring Works! See T5                                              | Combining      |
### Distributing the NOT
1. Invert every variable
2. Convert ANDs -> ORs and ORs -> ANDs
	- (NAND -> NOR, NOR -> NAND)
3. **MAINTAIN PRECEDENCE ORDER**

- If you apply a not to a whole eqn and distribute it, it’s called finding the DeMorgan Compliment

#### Example

```handwritten-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Writing/2026.1.9 - 13.43pm.writing"
}
```



