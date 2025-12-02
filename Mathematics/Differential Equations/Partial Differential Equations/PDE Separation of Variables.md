- One of the more common methods for solving simple [[Partial Differential Equations]]
- Can be easily used with [[The Heat Equation]] in 1D with no sources, [[The Wave Equation]] in 1D, and the 2D [[Laplace’s Equation]]

## Assumptions of the Method
We assume that a function of the following form will be a sol’n to a linear homogenous PDE in x and t:

```handwritten-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Writing/2025.11.14 - 13.27pm.writing"
}
```
This solution is called a **product solution**, and provided that the boundary conditions are linear and homogenous, it will satisfy them. 
- It will rarely satisfy the initial condition, but it DOES make it much easier to solve by splitting a PDE down to ODEs, which may then be separable.

It gets us a solution that states f(x) = g(t), which can only be true if they are both constant and equal. Thus, we get a solution f(x) = g(t) = -(lambda), where -(lambda) is an arbitrary **separation constant.**

### Steps
1. State your assumptions, specifically that of the form of the sol’n given above
2. Plug that sol’n in wherever you see u
3. Separate your variables, set equal to the separation constant
4. Split it into two equations, further separate to solve for your derivatives.
5. Check your boundary conditions
### Example

```handwritten-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Writing/2025.11.14 - 13.32pm.writing"
}
```
