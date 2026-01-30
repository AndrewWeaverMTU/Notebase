- A [[Surface Integrals|Surface Integral]] over a vector field
- Measures the flow through a surface, oriented with a **unit normal** vector to that surface. 
$$Flow = \int_D \int \vec{F} \cdot \vec{n} \space dS$$
```handwritten-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Writing/2025.11.17 - 8.24am.writing"
}
```

## Through a [[Parametric Surfaces|Parametric Surface]]
- **n = (Ru x Rv) / |Ru x Rv|** - unit normal vector
Flow through the surface:

$$ Flow = \int_D\int \vec{F}(\vec{r}(u, v)) \cdot \vec{r_u} \times \vec{r_v} \space dA$$

```handwritten-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Writing/2025.11.17 - 8.22am.writing"
}
```

### Example: flow through a Cylinder

```handwritten-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Writing/2025.11.17 - 8.36am.writing"
}
```


## Through a function Z = f(x,y)
- **n = <-Zx, -Zy, 1>** - normal vector.
$$Flow = \int_D\int\vec{F}(x,y,f(x,y))\cdot\langle-Z_x, -Z_y, 1\rangle dA$$
```handwritten-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Writing/2025.11.17 - 8.31am.writing"
}
```

## Through a Surface Parallel to a Coordinate Plane

$$Flow = \int_D\int\vec{F}(x,y,f(x,y))\cdot\vec{n} \space dA$$
$$\text{Where } \vec{n} \text{ is one of the following unit normal vectors: } \vec{n}_x = \langle 1, 0, 0\rangle; \vec{n}_y = \langle0,1,0\rangle; \vec{n}_z = \langle0,0,1\rangle$$
```handwritten-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Writing/2025.11.17 - 8.34am.writing"
}
```
