## The Dot Product

$$
\begin{bmatrix}
x_{1} \\
y_{1}
\end{bmatrix}
\cdot
\begin{bmatrix}
x_{2} \\
y_{2} 
\end{bmatrix}
= x_{1}x_{2}+y_{1}y_{2}
$$
Also sometimes called the scalar product.

Type: `Vector(a, n) -> Vector(a, n) -> a` (Assuming type `a` is closed under multiplication)

We can use this to calculate the length.
$$
|\vec{v}|=\sqrt{ \vec{v} \cdot \vec{v} } = \sqrt{ x^{2} + y^{2} }
$$
This norm is called the **modulus/length/norm**.
$$
\hat{v} = \frac{\vec{v}}{|\vec{v}|}
$$
$\hat{v}$ is a unit vector, and the process done above is called **normalizing**. We can now get the distance between two vectors $\vec{a}$ and $\vec{b}$ by taking $|\vec{a} - \vec{b}|$.

The dot product can also be written as follows -
$$
\vec{v}_{1}\cdot \vec{v}_{2} = |\vec{v}_{1}||\vec{v}_{2}|\cos \theta
$$
This gives us a nice formula for the angle between two vectors.
$$
\theta = \arccos\left( \frac{\vec{v}_{1}\cdot \vec{v}_{2}}{|\vec{v}_{1}||\vec{v}_{2}|} \right)
$$
The elements of a vector don't all have to be the same type. However, computing the dot product may not always be possible for such a vector.

The dot product of two orthogonal vectors is 0. Orthogonal vectors are said to be **maximally independent** of each other. The dot product can also be used as a measure of correlation/similarity.

The dot product is always $\geq 0$. This can be seen by the following -
$$
\vec{v}\cdot \vec{v} = \sum_{i=1}^{n} x^{2}_{i} \geq 0
$$
where $x_{i}$ is the $i$th element of the vector. This is why we can take square roots.

Important Note:
$$
\vec{a} \cdot \vec{b} = \vec{a} \cdot \vec{c} \nRightarrow \vec{b} = \vec{c}
$$
This is because we have not defined division. There are three ways this equation could be true, as is evident from the following rewritten equation.
$$
\vec{a} \cdot (\vec{b} - \vec{c}) = 0
$$
1. $\vec{a} = 0$
2. $\vec{b} - \vec{c} =0$
3. $\vec{a}$ is orthogonal to $\vec{b} - \vec{c}$.

We can also use dot products to find projections. Take a vector $\vec{v}$.
$$
\vec{v}\cdot \hat{x}=
\begin{bmatrix}
x \\
y
\end{bmatrix}\cdot \begin{bmatrix}
1 \\
0
\end{bmatrix} = |\vec{v}|\cdot |\hat{x}|\cdot \cos(\theta) = |\vec{v}|\cdot\cos(\theta)
$$
This is also a measure of correlation. Now, how do we find projections of a vector onto a non-basis vector?

$$
\vec{v} = L \frac{\vec{b}}{|\vec{b}|}
$$
$$
L = |\vec{a}|\cos \theta
$$
$$
\cos \theta =\frac{ \vec{a}\cdot \vec{b}}{|\vec{a}||\vec{b}|}
$$
Combining these, we get,
$$
\vec{v} = \frac{\vec{a}\cdot \vec{b}}{|\vec{b}|^{2}}\vec{b}
$$

An application of dot products can be seen in calculating work.
$$
W = \int \vec{F}\cdot d\vec{s}
$$

### Proving both formulas for dot product are equivalent.

$$
\vec{a}\cdot \vec{b} = \vec{a}\cdot(b_{1}\hat{e}_{1}+b_{2}\hat{e}_{2})
$$
We can now distribute the dot product over the sum. (It does that.)
$$
= b_{1}(\vec{a}\hat{e}_{1}) + b_{2}(\vec{a}\hat{e}_{2})
$$
The terms in the brackets are just projections.
$$
= b_{1}a_{1}+b_{2}a_{2}
$$

## Inner Products

A dot product is just an example of an inner product.

All inner products must have the following properties -
- The output must be a real number.
- The inner product must be commutative
- The inner product of the vector with itself must be $\geq 0$.
- The inner product should be linear.

These properties are slightly different when using complex numbers.
