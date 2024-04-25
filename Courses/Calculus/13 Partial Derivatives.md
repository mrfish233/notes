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
