# Multiple Integrals

## 14.1 Double and Iterated Integrals over Rectangles

### Theorem 1 - Fubini's Theorem (First Form)

If $f(x,y)$ is continuous throughout the rectangular region $R: a \le x \le b, c \le y \le d$, then

$$
\iint_{R} f(x,y) \ dA =
\int_{c}^{d} \int_{a}^{b} f(x,y) \ dx \ dy =
\int_{a}^{b} \int_{c}^{d} f(x,y) \ dy \ dx.
$$
## 14.2 Double Integrals over General Regions

### Theorem 2: Fubini's Theorem (Stronger Form)

Let $f(x,y)$ be continuous on a region $R$.

If $R$ is defined by $a \le x \le b$, $g_{1}(x) \le y \le g_{2}(x)$, with $g_{1}, g_{2}$ continuous on $[a,b]$, then

$$
\iint_{R} f(x,y) \ dA = 
\int_{a}^{b} \int_{g_{1}(x)}^{g_{2}(x)} f(x,y) \ dy \ dx.
$$

If $R$ is defined by $c \le y \le d$, $h_{1}(y) \le x \le h_{2}(y)$, with $h_{1}, h_{2}$ continuous on $[c,d]$, then

$$
\iint_{R} f(x,y) \ dA = 
\int_{c}^{d} \int_{h_{1}(x)}^{h_{2}(x)} f(x,y) \ dx \ dy.
$$

### Properties of Double Integrals

$$
\begin{align}
\text{1. } & \text{Constant Multiple} \\
\text{2. } & \text{Sum and Difference} \\
\text{3. } & \text{Domination:} \\
& (a) \iint_{R} f(x,y) \ dA \ge 0 \quad \text{if} \quad f(x,y) \ge 0 \text{ on } R \\
& (b) \iint_{R} f(x,y) \ dA \ge \iint_{R} g(x,y) \ dA \quad \text{if} \quad f(x,y) \ge g(x,y) \text{ on } R
\end{align}
$$

## 14.3 Area by Double Integration

### Definition: Area

The **area** of a closed, bounded plant region $R$ is

$$
A = \iint_{R} dA.
$$

### Average Value

The average value of $f$ over $R$ is

$$
\frac{1}{\text{area of} \ R} \iint_{R} f \ dA.
$$

## 14.4 Double Integrals in Polar Form

### Area in Polar Coordinates

The area of a closed and bounded region in $R$ in the polar coordinate plane is

$$
A = \iint_{R} r \ dr \ d\theta.
$$

### Changing Cartesian Integrals into Polar Integrals

$$
\iint_{R} f(x,y) \ dx \ dy
= \iint_{G} f(r \cos \theta, r \sin \theta) r \ dr \ d \theta.
$$

The region $G$ is same as region $R$, but described in polar coordinates.

## 14.5 Triple Integrals in Rectangular Coordinates

### Definition: Volume

The **volume** of a closed, bounded region $D$ in space is

$$
V = \iiint_{D} \ dV.
$$

### Average Value of a Function in Space

Average value of a function $F$ over a region $D$ in space is

$$
\frac{1}{\text{volume of }D} \iiint_{D} F \ dV.
$$

## 14.7 Triple Integrals in Cylindrical and Spherical Coordinates

### Definition: Cylindrical Coordinates

**Cylindrical coordinates** represent a point $P$ in space by ordered triples $(r, \theta, z)$ in which

1. $r$ and $\theta$ are polar coordinates for the vertical projection of $P$ on the $xy$-plane, with $r \ge 0$, and
2. $z$ is the rectangular vertical coordinate.

Equations Relating **Rectangular** and *Cylindrical Coordinates*:

$$
\begin{align}
&\text{1. } x = r \cos \theta \\
&\text{2. } y = r \sin \theta \\
&\text{3. } z = z \\
&\text{4. } r^{2} = x^{2} + y^{2} \\
&\text{5. } \tan \theta = \frac{y}{x} \\
\end{align}
$$

The triple integral of a function $f$ over $D$ is obtained by

$$
\iiint_{D} f \ r \ dz \ dr \ d \theta
$$

### Definition: Spherical Coordinates

![Spherical Coordinates](spherical_coordinates.png)

**Spherical coordinates** represent a point $P$ in space by ordered triples $(\rho, \phi, \theta)$ in which

1. $\rho$ is the *distance* from $P$ to the origin $(\rho \ge 0)$.
2. $\phi$ is the *angle* $\overset\rightharpoonup{OP}$ makes with the positive $z$-axis $(0 \le \phi \le \pi)$.
3. $\theta$ is the *angle* from cylindrical coordinates.

Equations Relating **Spherical Coordinates** to *Cartesian* and *Cylindrical Coordinates*:

$$
\begin{align}
&\text{1. } r = \rho \sin \phi \\
&\text{2. } z = \rho \cos \phi \\
&\text{3. } x = r \cos \theta = \rho \sin \phi \cos \theta \\
&\text{4. } y = r \sin \theta = \rho \sin \phi \sin \theta \\
&\text{5. } \rho = \sqrt{x^{2} + y^{2} + z^{2}} = \sqrt{r^{2} + z^{2}}. \\
\end{align}
$$

The triple integral is

$$
\iiint_{D} f(\rho, \phi, \theta) \ dV =
\iiint_{D} f(\rho, \phi, \theta) \rho^{2} \sin{\phi} \ d\rho \ d\phi \ d\theta
$$

### Summary

**Coordinate Conversion Formulas**

1. Cylindrical to Rectangular

$$
\begin{align}
x &= r \cos \theta \\
y &= r \sin \theta \\
z &= z
\end{align}
$$

2. Spherical to Rectangular

$$
\begin{align}
x &= \rho \sin \phi \cos \theta \\
y &= \rho \sin \phi \sin \theta \\
z &= \rho \cos \phi
\end{align}
$$

3. Spherical to Cylindrical

$$
\begin{align}
r &= \rho \sin \theta \\
z &= \rho \cos \theta \\
\theta &= \theta
\end{align}
$$

**Corresponding formula for $dV$ in triple integrals:**

$$
\begin{align}
dV &= dx \ dy \ dz \\
&= r \ dz \ dr \ d\theta \\
&= \rho^{2} \sin \phi \ d\rho \ d\phi \ d\theta
\end{align}
$$

## 14.8 Substitutions in Multiple Integrals

### Definition: Jacobian determinant

The **Jacobian determinant** or Jacobian of the coordinate transformation $x = g(u,v), y = h(u,v)$ is

$$
J(u,v) =
\frac{\delta(x,y)}{\delta(u,v)} =
\begin{vmatrix}
\displaystyle\frac{\delta x}{\delta u} & \displaystyle\frac{\delta x}{\delta v} \\
\displaystyle\frac{\delta y}{\delta u} & \displaystyle\frac{\delta y}{\delta v}
\end{vmatrix} =
\frac{\delta x}{\delta u} \frac{\delta y}{\delta v} - \frac{\delta y}{\delta u} \frac{\delta x}{\delta v}.
$$

### Theorem 3: Substitution for Double Integrals

Suppose that $f(x,y)$ is continuous over the region $R$. Let $G$ be the preimage of $R$ under the transformation $x = g(u,v), y = h(u,v)$, which is assumed to be one-to-one on the interior of $G$.

If $g, h$ have continuous first partial derivatives within the interior of $G$, then

$$
\iint_{R} f(x,y) \ dx \ dy =
\iint_{G} f(g(u,v), h(u,v)) \left|\frac{\delta(x,y)}{\delta(u,v)}\right| \ du \ dv.
$$

### Substitutions in Triple Integrals

Suppose that a region $G$ in $uvw$-space is transformed one-to-one into the region $D$ in $xyz$-space by differentiable equations of the form

$$
x = g(u,v,w), \quad y = h(u,v,w), \quad z = k(u,v,w),
$$

then any function $F(x,y,z)$ defined on $D$ can be thought of as a function

$$
F(g(u,v,w), h(u,v,w), k(u,v,w)) = H(u,v,w)
$$

defined on $G$. If $g, h, k$ have continuous first partial derivatives, then the integral of $F(x,y,z)$ over $D$ is related to the integral of $H(u,v,w)$ over $G$ by the equation

$$
\iiint_{D} F(x,y,z) \ dx \ dy \ dz =
\iiint_{G} H(u,v,w) \ |J(u,v,w)| \ du \ dv \ dw.
$$

The factor $J(u,v,w)$, is the **Jacobian determinant**

$$
J(u,v,w) = 
\begin{vmatrix}
\displaystyle\frac{\delta x}{\delta u} & \displaystyle\frac{\delta x}{\delta v} & \displaystyle\frac{\delta x}{\delta w} \\
\displaystyle\frac{\delta y}{\delta u} & \displaystyle\frac{\delta y}{\delta v} & \displaystyle\frac{\delta y}{\delta w} \\
\displaystyle\frac{\delta y}{\delta u} & \displaystyle\frac{\delta y}{\delta v} & \displaystyle\frac{\delta z}{\delta w}
\end{vmatrix} =
\frac{\delta (x,y,z)}{\delta (u,v,w)}.
$$
