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

**Spherical coordinates** represent a point $P$ in space by ordered triples $(\rho, \phi, \theta)$ in which

1. $\rho$ is the distance from $P$ to the origin $(\rho \ge 0)$.
2. $\phi$ is the angle $\overset\rightharpoonup{OP}$ makes with the positive $z$-axis $(0 \le \phi \le \pi)$.
3. $\theta$ is the angle from cylindrical coordinates.

Equations Relating **Spherical Coordinates** to *Cartesian* and *Cylindrical Coordinates*:

$$
\begin{align}
&\text{1. } r = \rho \sin \theta \\
&\text{2. } z = \rho \cos \theta \\
&\text{3. } x = r \cos \theta = \rho \sin \theta \cos \theta \\
&\text{4. } r^{2} = x^{2} + y^{2} \\
&\text{5. } \tan \theta = \frac{y}{x} \\
\end{align}
$$
