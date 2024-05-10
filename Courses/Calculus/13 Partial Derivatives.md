# Partial Derivatives

## 13.1 Functions of Several Variables

### Definition 1 - Function of Several Variables

Suppose $D$ is a set of $n$-tuples of real numbers $(x_{1}, x_{2}, \cdots, x_{n})$. A **real-valued function** $f$ on $D$ is a rule that assigns a real number

$$
w = f(x_{1}, x_{2}, \cdots, x_{n})
$$

to each element in $D$. The set $D$ is the function's **domain**. The set of $w$-values taken on by $f$ is the function's **range**.

$w$ is the **dependent variable** of $f$, and $f$ is the function of the $n$ **independent variables** $x_{1}$ to $x_{n}$.

### Definition 2 - Interior Points and Boundary Points

A point $(x_{0}, y_{0})$ in a region $R$ in the $xy$-plane is an **interior point** of $R$ if it is the center of a disk of positive radius that lies entirely in $R$. A point is a **boundary point** of $R$ if every disk centered at $(x_{0}, y_{0})$ contains points that lie outside of $R$ as well as points that lie in $R$.

The interior points of a region, as a set, make up the **interior** of the region. The region's boundary points make up its **boundary**. A region is **open** if it consists entirely of interior points. A region is **closed** if it contains all its boundary points.

### Definition 3 - Bounded and Unbounded Region

A region in the plane is **bounded** if it lies inside a disk of finite radius. A region is **unbounded** if it is not bounded.

### Definition 4 - Graphs and Curves

The set of points in the plane where a function $(x, y)$ has a constant value

$$
z = f(x,y)
$$

is called a **level curve** of $f$. The set of all points

$$
(x, y, f(x,y))
$$

in space, for $(x,y)$ in the domain of $f$, is called the **graph** of $f$.

The graph of $f$ is often called the **surface** $z = f(x,y)$.

## 13.2 Limits and Continuity in Higher Dimensions

### Definition 6 - Limits for Functions of Two Variables

Suppose that every open circular disk centered at $(x_{0}, y_{0})$ contains a point in the domain of $f$ other than $(x_{0}, y_{0})$ itself. If for every number $\varepsilon > 0$, there exists a corresponding number $\delta > 0$ such that

$$
\forall (x,y) \in D, \quad |f(x,y) - L| < \varepsilon \quad
\text{whenever} \quad
0 < \sqrt{(x-x_{0})^{2} + (y-y_{0})^{2}} < \delta,
$$

then we say that a function $f(x,y)$ approaches the **limit** $L$ as $(x,y)$ approaches $(x_{0}, y_{0})$, and write

$$
\lim_{(x,y) \to (x_{0},y_{0})} f(x,y) = L.
$$

### Theorem 1 - Properties of Limits of Functions of Two Variables

If $L, M, k$ are real numbers and

$$
\lim_{(x,y) \to (x_{0},y_{0})} f(x,y) = L
\quad \text{and} \quad
\lim_{(x,y) \to (x_{0},y_{0})} g(x,y) = M.
$$

Then

$$
\begin{align}
1. &\text{Sum Rule: } \quad &&\lim_{(x,y) \to (x_{0},y_{0})} [f(x,y) + g(x,y)] = L + M \\
2. &\text{Difference Rule: } \quad &&\lim_{(x,y) \to (x_{0},y_{0})} [f(x,y) - g(x,y)] = L - M \\
3. &\text{Constant Multiple Rule: } \quad &&\lim_{(x,y) \to (x_{0},y_{0})} [k \cdot f(x,y)] = kL \\
4. &\text{Product Rule: } \quad &&\lim_{(x,y) \to (x_{0},y_{0})} [f(x,y) \cdot g(x,y)] = L \cdot M \\
5. &\text{Quotient Rule: } \quad &&\lim_{(x,y) \to (x_{0},y_{0})} \frac{f(x,y)}{g(x,y)} = \frac{L}{M}, \quad M \ne 0 \\
6. &\text{Power Rule: } \quad &&\lim_{(x,y) \to (x_{0},y_{0})} [f(x,y)]^{n} = L^{n}, \quad n \in \mathbb{Z}^{+} \\
7. &\text{Root Rule: } \quad &&\lim_{(x,y) \to (x_{0},y_{0})} \sqrt[n]{f(x,y)}  = \sqrt[n]{L}, \quad n \in \mathbb{Z}^{+} \\
8. &\text{Composition Rule: } \quad &&\lim_{(x,y) \to (x_{0},y_{0})} h(f(x,y))  = h(L).\\
\end{align}
$$

Note in rule 7: if $n$ is even, we assume that $L > 0$.
Note in rule 8: $h(z)$ is continuous at $z = L$.

### Definition 7 - Continuity of Functions

Suppose that every open circular disk centered at $(x_{0}, y_{0})$ contains a point in the domain of $f$ other than $(x_{0}, y_{0})$ itself. Then a function $f(x, y)$ is **continuous at the point** $(x_{0}, y_{0})$ if $f$ is defined at $(x_{0}, y_{0})$, and

$$
\lim_{(x,y) \to (x_{0},y_{0})} f(x,y) = f(x_{0}, y_{0}).
$$

A function is **continuous** if it is continuous at every point of its domain.

### Two-Path Test for Nonexistence of a Limit

If a function $f(x,y)$ has different limits along two different paths in the domain of $f$ as $(x,y)$ approaches $(x_{0}, y_{0})$, then the following limit **does not exist**:

$$
\lim_{(x,y) \to (x_{0},y_{0})} f(x,y)
$$

Having the same limit along all straight lines approaching $(x_{0}, y_{0})$ does not imply that a limit exists at $(x_{0}, y_{0})$.

### Continuity of Compositions

If $f$ is continuous at $(x_{0}, y_{0})$ and $g$ is a single-variable function continuous at $f(x_{0}, y_{0})$, then the composition $h = g \circ f$ defined by

$$
h(x,y) = g(f(x,y))
$$

is also continuous at $(x_{0}, y_{0})$.

## 13.3 Partial Derivatives

### Definition 8 - Partial Derivative

The **partial derivative** of $f(x,y)$ with respect to $x$ at the point $(x_{0}, y_{0})$ is

$$
\left. \frac{\delta f}{\delta x} \right |_{(x_{0}, y_{0})} =
\left. \frac{d}{dx} f(x, y_{0}) \right |_{x = x_{0}} =
\lim_{h \to 0} \frac{f(x_{0} + h, y_{0}) - f(x_{0}, y_{0})}{h},
$$

provided the limit exists.

### Theorem 2 - The Mixed Derivative Theorem

If $f(x, y)$ and its partial derivatives $f_{x}, f_{y}, f_{xy}, f_{yx}$ are **defined** throughout an open region containing a point $(a, b)$ and are all **continuous** at $(a, b)$, then

$$
f_{xy}(a, b) = f_{yx}(a, b).
$$

**Note:** the order of mixed partial derivatives are defined as below:

$$
\frac{\delta^{2}f}{\delta x \delta y} = 
\frac{\delta}{\delta x} \left(\frac{\delta f}{\delta y}\right) =
f_{yx} = (f_{y})_{x},
$$

means differentiate **first** with respect to $y$, then with respect with $x$.

### Definition 9 - Differentiability

A function $z = f(x, y)$ is **differentiable at** $(x_{0}, y_{0})$ if $f_{x}(x_{0}, y_{0})$ and $f_{y}(x_{0}, y_{0})$ exist and $\Delta z = f(x_{0} + \Delta x, y_{0} + \Delta y) - f(x_{0}, y_{0})$ satisfies an equation of the form

$$
\Delta z = f_{x}(x_{0}, y_{0}) \Delta x + f_{y}(x_{0}, y_{0}) \Delta y + \varepsilon_{1} \Delta x + \varepsilon_{2} \Delta y,
$$

in which $\varepsilon_{1}, \varepsilon_{2} \to 0$ as $\Delta x, \Delta y \to 0$. We call $f$ **differentiable** if it is differentiable at every point in its domain, and say that its graph is a smooth curve.

### Theorem 3 - The Increment Theorem

Suppose $f_{x}, f_{y}$ are defined throughout an open region $R$ containing the point $(x_{0}, y_{0})$ and that $f_{x}, f_{y}$ are continuous at $(x_{0}, y_{0})$, then the change

$$
\Delta z = f(x_{0} + \Delta x, y_{0} + \Delta y) - f(x_{0}, y_{0})
$$

in the value of $f$ that results from moving from $(x_{0}, y_{0})$ to another point $(x_{0} + \Delta x, y_{0} + \Delta y)$ in $R$ satisfies an equation of the form

$$
\Delta z = f_{x}(x_{0}, y_{0}) \Delta x + f_{y}(x_{0}, y_{0}) \Delta y + \varepsilon_{1} \Delta x + \varepsilon_{2} \Delta y
$$

in which $\varepsilon_{1}, \varepsilon_{2} \to 0$ as $\Delta x, \Delta y \to 0$.

#### Corollary 3

If the partial derivatives $f_x$ and $f_y$ of a function $f(x, y)$ are continuous throughout an open region $R$, then $f$ is **differentiable** at every point of $R$.

### Theorem 4 - Differentiability Implies Continuity

If a function $f(x, y)$ is differentiable at $(x_{0}, y_{0})$, then $f$ is **continuous** at $(x_{0}, y_{0})$.

## 13.4 Chain Rule

### Theorem 5 - Chain Rule

For functions of 1 independent variable and 2 intermediate functions:

If $z = f(x, y)$ is differentiable and if $x = x(t), y = y(t)$ are differentiable functions of $t$, then the composition $z = f(x(t), y(t))$ is a differentiable function of $t$ and

$$
\begin{align}
\frac{dz}{dt} &= f_{x}(x(t), y(t)) x'(t) + f_{y}(x(t), y(t)) y'(t) \\
&= \frac{\delta f}{\delta x} \frac{dx}{dt} + \frac{\delta f}{\delta y} \frac{dy}{dt}.
\end{align}
$$

### Theorem 8 - Implicit Differentiation

Suppose that $F(x, y)$ is differentiable and that the equation $F(x, y) = 0$ defines $y$ as a differentiable function of $x$, then at any point where $F_{y} \ne 0$,

$$
\frac{dy}{dx} = - \frac{F_{x}}{F_{y}}.
$$

**Proof:**

Let $w = F(x, h(x))$ where $y = h(x)$, then since $F(x, h(x)) = 0$, we have

$$
\frac{dw}{dx} = F_{x} \frac{dx}{dx} + F_{y} \frac{dy}{dx} = 0.
$$

If $F_{y} \ne 0$, then

$$
\frac{dy}{dx} = - \frac{F_{x}}{F_{y}}.
$$

**Example:** $y^{2} - x^{2} - \sin{xy} = 0$.

Let $F(x,y) = y^{2} - x^{2} - \sin{xy}$, then

$$
\frac{dy}{dx} = - \frac{F_{x}}{F_{y}}
= - \frac{-2x - y \cos{xy}}{2y - x \cos{xy}}
= \frac{2x + y \cos{xy}}{2y - x \cos{xy}}
$$

## 13.5 Directional Derivatives and Gradient Vectors

### Definition 10 - Directional Derivative

The derivative of $f$ at $P_{0}(x_{0}, y_{0})$ in the direction of the unit vector $\mathbf{u} = u_{1} \mathbf{i} + u_{2} \mathbf{j}$ is the number

$$
\left(\frac{df}{ds}\right)_{\mathbf{u}, \ P_{0}} =
\lim_{s \to 0} \frac{f(x_{0} + su_{1}, y_{0} + su_{2}) - f(x_{0}, y_{0})}{s},
$$

provided the limit exists. The **directional derivative** is also defined by

$$
D_{\mathbf{u}} f(P_{0}) \quad \text{or} D_{\mathbf{u}}f |_{P_{0}}
$$

**Example:** find the derivative of

$$
f(x, y) = x^{2} + xy
$$

at $P_{0}(1, 2)$ in the direction of the unit vector $\mathbf{u} = (1/\sqrt{2})\mathbf{i} + (1/\sqrt{2})\mathbf{j}.$

$$
\begin{align}
\left(\frac{df}{ds}\right)_{\mathbf{u}, \ P_{0}} &=
\lim_{s \to 0} \frac{f(x_{0} + su_{1}, y_{0} + su_{2}) - f(x_{0}, y_{0})}{s} \\
&= \lim_{s \to 0} \frac{f\left(1 + \frac{s}{\sqrt{2}}, 2 + \frac{s}{\sqrt{2}}\right) - f(1, 2)}{s} \\
&= \cdots \\
&= \lim_{s \to 0} \left(\frac{5}{\sqrt{2}} + s\right) \\
&= \frac{5}{\sqrt{2}}.
\end{align}
$$

### Definition 11 - Gradient Vector

The **gradient vector** (or **gradient**) of $f(x, y)$ is the vector

$$
\nabla f = \frac{\delta f}{\delta x} \mathbf{i} + \frac{\delta f}{\delta y} \mathbf{j}.
$$

The value of the gradient vector obtained by evaluating the partial derivatives at a point $P_{0} (x_{0}, y_{0})$ is written

$$
\nabla f \mid_{P_{0}} \quad \text{or} \quad \nabla f(x_{0}, y_{0}).
$$

### Theorem 9 - Directional Derivative is a Dot Product

If $f(x, y)$ is differentiable in an open region containing $P_{0}(x_{0}, y_{0})$, then

$$
\left(\frac{df}{ds}\right)_{\mathbf{u}, \ P_{0}} =
\nabla f \mid_{P_{0}} \cdot \mathbf{u}.
$$

**Example:** find the derivative of $f(x, y) = xe^{y} + \cos{xy}$ at the point $(2, 0)$ in the direction of $\mathbf{v} = 3 \mathbf{i} + 4 \mathbf{j}$.

We have

$$
\mathbf{u} = \frac{\mathbf{v}}{|\mathbf{v}|} = \frac{\mathbf{v}}{5} =
\frac{3}{5} \mathbf{i} - \frac{4}{5} \mathbf{j}.
$$

And the partial derivatives of $f$ at $(2, 0)$ are

$$
\begin{align}
f_{x}(2, 0) &= \left. (e^{y} - y \sin xy) \right|_{(2, 0)} = 1 \\
f_{y}(2, 0) &= \left. (x e^{y} - x \sin xy) \right|_{(2, 0)} = 2
\end{align}
$$

The gradient of $f$ at $(2, 0)$ is

$$
\nabla f |_{(2, 0)} = f_{x}(2, 0) \mathbf{i} + f_{y} (2, 0) \mathbf{j} = \mathbf{i} + 2\mathbf{j}
$$

Therefore the derivative of $f$ at $(2, 0)$ in direction of $\mathbf{v}$ is

$$
\begin{align}
D_{\mathbf{u}}f|_{(2, 0)} &= \nabla f|_{(2, 0)} 
\cdot \mathbf{u} \\
&= (\mathbf{i} + 2\mathbf{j}) \cdot \left(\frac{3}{5} \mathbf{i} - \frac{4}{5} \mathbf{j}\right) \\
&= \frac{3}{5} - \frac{8}{5} \\
&= -1.
\end{align}
$$

### Properties of the Directional Derivative

$$
D_{\mathbf{u}}f = \nabla f \cdot \mathbf{u}
= | \nabla f | | \mathbf{u} | \cos \theta
= | \nabla f | \cos \theta
$$

1. The function $f$ **increases most rapidly** when $\cos \theta = 1$, or $\theta = 0$. That is, $f$ increases most rapidly in the direction of the gradient vector $\nabla f$ at $P$. The derivative in this direction is

$$
D_{\mathbf{u}}f = | \nabla f | \cos 0 = | \nabla f |.
$$

2. The function $f$ **decreases most rapidly** in the direction of $- \nabla f$. The derivative in this direction is

$$
D_{\mathbf{u}}f = | \nabla f | \cos \pi = | \nabla f |.
$$

3. Any direction $\mathbf{u}$ orthogonal to a gradient $\nabla f \ne 0$ is a direction of zero change in $f$ because $\theta = \displaystyle\frac{\pi}{2}$ and

$$
D_{\mathbf{u}}f = | \nabla f | \cos \frac{\pi}{2} = 0.
$$

### Equation for the Tangent Line to a Level Curve

$$
f_{x} (x_{0}, y_{0}) (x - x_{0}) + f_{y} (x_{0}, y_{0}) (y - y_{0}) = 0
$$

**Example:** find an equation for the tangent to the ellipse

$$
f(x, y) = \frac{x^{2}}{4} + y^{2}
$$

at the point $(-2, 1)$.

The gradient of $f$ at $(-2, 1)$ is

$$
\nabla f |_{(-2, 1)} = \left. \left(\frac{x}{2} \mathbf{i} + 2y \mathbf{j}\right) \right|_{(-2, 1)} = -\mathbf{i} + 2\mathbf{j}
$$

Because this gradient vector is nonzero, the tangent to the ellipse at $(-2, 1)$ is the line

$$
\begin{align}
f_{x}(-2, 1) (x + 2) + f_{y}(-2, 1) (x - 1) &= 0 \\
x - 2y &= 4.
\end{align}
$$

### Algebra Rules for Gradients

$$
\begin{align}
1. &\text{Sum Rule: } \quad &&\nabla (f + g) &&= \nabla f + \nabla g \\
2. &\text{Difference Rule: } \quad &&\nabla (f - g) &&= \nabla f - \nabla g \\
3. &\text{Constant Multiple Rule: } \quad &&\nabla (kf) &&= k \nabla f \\
4. &\text{Product Rule: } \quad &&\nabla (fg) &&= f \nabla g + g \nabla f \\
5. &\text{Quotient Rule: } \quad &&\nabla \left(\frac{f}{g}\right) &&= \frac{g \nabla f - f \nabla g}{g^{2}} \\
\end{align}
$$

## 13.6 Tangent Planes and Differentials

### Definition 12 - Tangent Plane

The **tangent plane** to the level surface $f(x, y, z) = c$ of a differentiable function $f$ at a point $P_{0}$ where the gradient is not zero is the plane through $P_{0}$ normal to $\nabla f |_{P_{0}}$. The tangent plane to $f(x,y,z) = c$ at $P_{0}(x_{0}, y_{0}, z_{0})$ is

$$
f_{x}(P_{0})(x - x_{0}) + f_{y}(P_{0})(y - y_{0}) + f_{z}(P_{0})(z - z_{0}) = 0.
$$

The **normal line** of the surface at $P_{0}$ is the line through $P_{0}$ parallel to $\nabla f |_{P_{0}}$. The normal line to $f(x,y,z) = c$ at $P_{0}(x_{0}, y_{0}, z_{0})$ is

$$
x = x_{0} + f_{x}(P_{0})t,
\quad y = y_{0} + f_{y}(P_{0})t,
\quad z = z_{0} + f_{z}(P_{0})t.
$$

### Plane Tangent to Surface $z = f(x,y)$

The plane tangent to the surface $z = f(x,y)$ of a differentiable function $f$ at the point $P_{0}(x_{0}, y_{0}, f(x_{0}, y_{0}))$ is

$$
f_{x}(x_{0}, y_{0})(x - x_{0}) + f_{y}(x_{0}, y_{0})(y - y_{0}) - (z - z_{0}) = 0.
$$

### Estimating the Change in $f$ in Direction $u$

To estimate the change in function $f$ when moving a small distance $ds$ from a point $P_{0}$ in a particular direction $\mathbf{u}$,

$$
df = (\nabla f |_{P_{0}} \cdot \mathbf{u}) \ ds
$$

**Example:** $f(x,y,z) = y \sin x + 2yz$, from $P_{0}(0,1,0)$ to $P_{1}(2,2,-2)$, moves $0.1$ unit.

Since

$$
\overrightarrow{P_{0}P_{1}} = 2 \mathbf{i} + \mathbf{j} - 2 \mathbf{k},
$$

the unit vector is

$$
\mathbf{u} = \frac{\overrightarrow{P_{0}P_{1}}}{|\overrightarrow{P_{0}P_{1}}|} = \frac{2}{3} \mathbf{i} + \frac{1}{3} \mathbf{j} - \frac{2}{3} \mathbf{k}. 
$$

The gradient of $f$ at $P_{0}$ is

$$
\nabla f |_{(0,1,0)} = ((y \cos x) \mathbf{i} + (\sin x + 2z) \mathbf{j} + 2y \mathbf{k}) |_{(0,1,0)} = \mathbf{i} + 2\mathbf{k}.
$$

Therefore

$$
\nabla f |_{P_{0}} \cdot \mathbf{u} = (\mathbf{i} + 2\mathbf{k}) \cdot \left(\frac{2}{3} \mathbf{i} + \frac{1}{3} \mathbf{j} - \frac{2}{3} \mathbf{k}\right) = -\frac{2}{3}.
$$

The change $df$ is approximately

$$
df = \left(- \frac{2}{3}\right) (ds) \approx -0.067 \ \text{unit}.
$$

### Definition 13 - Linearization

The **linearization** of a function $f(x,y)$ at a point $(x_{0}, y_{0})$ where $f$ is differentiable is the function

$$
L(x,y) = f(x_{0}, y_{0}) + f_{x}(x_{0}, y_{0})(x - x_{0}) + f_{y}(x_{0}, y_{0})(y - y_{0}).
$$

The approximation

$$
f(x,y) \approx L(x,y)
$$

is the **standard linear approximation** of $f$ at $(x_{0}, y_{0})$.

### Error in Standard Linear Approximation

If $f$ has continuous first and second partial derivatives throughout an open set containing a rectangle $R$ centered at $(x_{0}, y_{0})$, and if $M$ is any upper bound for the values of $|f_{xx}|, |f_{yy}|, |f_{xy}|$ on $R$, then the error $E(x,y)$ incurred in replacing $f(x,y)$ on $R$ by its linearization

$$
L(x,y) = f(x_{0}, y_{0}) + f_{x}(x_{0}, y_{0})(x - x_{0}) + f_{y}(x_{0}, y_{0})(y - y_{0})
$$

satisfies the inequality

$$
|E(x,y)| \le \frac{1}{2} M (|x - x_{0}| + |y - y_{0}|)^{2}.
$$

### Definition 14 - Total Differential

If we move from $(x_{0}, y_{0})$ to a point $(x_{0} + dx, y_{0} + dy)$ nearby, the resulting change

$$
df = f_{x}(x_{0}, y_{0}) \ dx + f_{y}(x_{0}, y_{0}) \ dy
$$

in the linearization of $f$ is called the **total differential** of $f$.

## 13.7 Extreme Values and Saddle Points

### Definition 15 - Local Maximum / Minimum

Let $f(x,y)$ be defined on a region $R$ containing the point $(a,b)$, then

1. $f(a,b)$ is a **local maximum** value of $f$ if $f(a,b) \ge f(x,y)$ for all domain points $(x,y)$ in an open disk centered at $(a,b)$.
2. $f(a,b)$ is a **local minimum** value of $f$ if $f(a,b) \le f(x,y)$ for all domain points $(x,y)$ in an open disk centered at $(a,b)$.

If such points exist, the tangent planes are horizontal. Local maxima are also called **relative extrema**.

### Theorem 10 - First Derivative Theorem for Local Extreme Values

If $f(x,y)$ has a *local maximum or minimum value* at an interior point $(a,b)$ of its domain and if the first partial derivatives exist there, then

$$
f_{x}(a,b) = 0 \quad \text{and} \quad f_{y}(a,b) = 0.
$$

**Proof:**

If $f$ has local extremum at $(a,b)$, then the function $g(x) = f(x,b)$ has a local extremum at $x = a$. Therefore, $g'(a) = f_{x}(a,b) = 0$. Similarly, $f_{y}(a,b) = 0$.

Substitute $f_{x}(a,b) = 0$ and $f_{y}(a,b) = 0$ into the equation of tangent plane to the surface at $(a,b)$:

$$
\begin{align}
f_{x}(a,b)(x-a) + f_{y}(a,b)(y-b) - (z - f(a,b)) &= 0 \\
0 \cdot (x-a) + 0 \cdot (y-b) - (z - f(a,b)) &= 0
\end{align}
$$

The equation reduces to

$$
z = f(a,b).
$$

Thus, the surface has a horizontal tangent plane at a local extremum, provided there's a tangent plane there.

### Definition 16 - Critical Point

An interior point of the domain of a function $f(x,y)$ where both $f_{x}, f_{y}$ are zero or where one or both of $f_{x}$ and $f_{y}$ do not exist is a **critical point** of $f$.

### Definition 17 - Saddle Point

A differentiable function $f(x,y)$ has a **saddle point** at a critical point $(a,b)$ if in every open disk centered at $(a,b)$ there are domain points $(x,y)$ where $f(x,y) > f(a,b)$ and $f(x,y) < f(a,b)$.

### Theorem 11 - Second Derivative Test for Local Extreme Values

Suppose that $f(x,y)$ and its first and second partial derivatives are continuous throughout a disk centered at $(a,b)$ and that $f_{x}(a,b) = f_{y}(a,b) = 0$, then

1. $f$ has a **local maximum** at $(a,b)$ if $f_{xx} < 0$ and $f_{xx}f_{yy} - f_{xy}^{2} > 0$ at $(a,b)$.
2. $f$ has a **local minimum** at $(a,b)$ if $f_{xx} > 0$ and $f_{xx}f_{yy} - f_{xy}^{2} > 0$ at $(a,b)$.
3. $f$ has a **saddle point** at $(a,b)$ if $f_{xx}f_{yy} - f_{xy}^{2} < 0$ at $(a,b)$.
4. The test is **inconclusive** at $(a,b)$ if $f_{xx}f_{yy} - f_{xy}^{2} = 0$ at $(a,b)$.

The expression $f_{xx}f_{yy} - f_{xy}^{2} > 0$ is called the *discriminant* or *Hessian* of $f$.

$$
f_{xx}f_{yy} - f_{xy}^{2} = 
\begin{vmatrix}
f_{xx} & f_{xy} \\
f_{yx} & f_{yy}
\end{vmatrix}.
$$

### Absolute Maxima and Minima on Closed Bounded Regions

To find absolute extrema of a function $f(x,y)$ on a closed and bounded region $R$,

1. List the **interior points** of $R$ where $f$ may have local maxima and minima and evaluate $f$ at these points. These are *critical points* if $f$.
2. List the **boundary points** of $R$ where $f$ has local maxima and minima and evaluate $f$ at these points.
3. Look through the lists for the maximum and minimum values of $f$. These will be the *absolute maximum and minimum* values of $f$ on $R$.

## 13.8 Lagrange Multipliers

### Theorem 12 - The Orthogonal Gradient Theorem

Suppose that $f(x,y,z)$ is differentiable in a region whose interior contains a smooth curve

$$
C: r(t) = x(t) \mathbf{i} + y(t) \mathbf{j} + z(t) \mathbf{k}.
$$

If $P_{0}$ is a point on $C$ where $f$ has a local maximum or minimum relative to its values on $C$, then $\nabla f$ is orthogonal to the curve's tangent vector $\mathbf{r}'$ at $P_{0}$.

#### Corollary of Theorem 12

At the points on a smooth curve $\mathbf{r}(t) = x(t) \mathbf{i} + y(t) \mathbf{j}$ where a differentiable function $f(x,y)$ takes on its local maxima and minima relative to its values on the curve, we have $\nabla{f} \cdot \mathbf{r}' = 0$.

### Method of Lagrange Multipliers

Suppose that $f(x,y,z)$ and $g(x,y,z)$ are differentiable and $\nabla{g} \ne 0$ when $g(x,y,z) = 0$. To find the local maximum and minimum values of $f$ subject to the constraint $g(x,y,z) = 0$, find the values of $x, y, z, \lambda$ that satisfy the equation

$$
\nabla{f} = \lambda \nabla{g}
\quad \text{and} \quad
g(x,y,z) = 0.
$$

**Example:** find the largest and smallest values that the function

$$
f(x,y) = xy
$$

takes on the ellipse

$$
\frac{x^{2}}{8} + \frac{y^{2}}{2} = 1.
$$

**Solution:**

Let

$$
g(x,y) = \frac{x^{2}}{8} + \frac{y^{2}}{2} - 1 = 0,
$$

then find the values of $x, y, \lambda$ for which

$$
\nabla{f} = \lambda \nabla{g}
\quad \text{and} \quad
g(x,y) = 0.
$$

Then

$$
\begin{align}
\nabla{f} &= \lambda \nabla{g} \\
y \mathbf{i} + x \mathbf{j} &= \frac{\lambda}{4} x \mathbf{i} + \lambda y \mathbf{j},
\end{align}
$$

we find that $y = \frac{\lambda}{4}x, x = \lambda y$, or $y = \frac{\lambda^{2}}{4}y$, so that $y = 0$ or $\lambda = \pm 2$. Consider two cases:

*Case 1:* If $y = 0$, then $x = y = 0$, but $(0,0)$ is not on the ellipse. Hence $y \ne 0$.

*Case 2:* If $y \ne 0$, then $\lambda = \pm 2$ and $x = \pm 2y$. Substituting this into $g(x,y) = 0$ gives

$$
\begin{align}
\frac{(\pm 2y)^{2}}{8} + \frac{y^{2}}{2} &= 1 \\
4y^{2} + 4y^{2} &= 8 \\
y &= \pm 1.
\end{align}
$$

The function $f(x,y) = xy$ therefore takes on its extreme values on the ellipse at the four points $(\pm 2, \pm 1)$. The extreme values are $xy = 2$ and $xy = -2$.

### Lagrange Multipliers with Two Constraints

To find the extreme values of a differentiable function $f(x,y,z)$ with two constraints

$$
g_{1}(x,y,z) = 0, \quad g_{2}(x,y,z) = 0
$$

and $g_{1}, g_{2}$ are differentiable and not parallel to each other, we need to find the values of $x, y, z, \lambda, \mu$ that satisfy the equation

$$
\nabla{f} = \lambda \nabla{g_{1}} + \mu \nabla{g_{2}},
\quad g_{1}(x,y,z) = 0,
\quad g_{2}(x,y,z) = 0.
$$

**Example:** The plane $x + y + z = 1$ cuts the cylinder $x^{2} + y^{2} = 1$ in an ellipse, find the points on the ellipse that lie closest to and farthest from the origin.

**Solution:**

We need to find the values of

$$
f(x,y,z) = x^{2} + y^{2} + z^{2}
$$

subject to the constraints

$$
\begin{align}
g_{1}(x,y,z) &= x^{2} + y^{2} - 1 = 0 \\
g_{2}(x,y,z) &= x + y + z - 1 = 0.
\end{align}
$$

The gradient equation gives

$$
\begin{align}
\nabla{f} &= \lambda \nabla{g_{1}} + \mu \nabla{g_{2}} \\
2x \mathbf{i} + 2y \mathbf{j} + 2z \mathbf{k} &= 
\lambda (2x \mathbf{i} + by \mathbf{j}) + \mu (\mathbf{i} + \mathbf{j} + \mathbf{k}) \\
&= (2 \lambda x + \mu) \mathbf{i} + (2 \lambda y + \mu) \mathbf{j} + \mu \mathbf{k},
\end{align}
$$

or

$$
2x = 2 \lambda x + \mu, \quad 2y = 2 \lambda y + \mu, \quad 2z = \mu.
$$

Therefore we need to solve

$$
\begin{cases}
g_{1}(x,y,z) = x^{2} + y^{2} - 1 = 0 \\
g_{2}(x,y,z) = x + y + z - 1 = 0 \\
2x = 2 \lambda x + \mu \\
2y = 2 \lambda y + \mu \\
2z = \mu
\end{cases}
$$
