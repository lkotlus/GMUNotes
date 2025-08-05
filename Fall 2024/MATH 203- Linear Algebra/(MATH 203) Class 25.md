### The penultimate class
- So sad.

### Orthogonal projection bases
- We've introduced projections: $$\text{proj}_L\left(\overrightarrow{y}\right)=\frac{\overrightarrow{u}\cdot\overrightarrow{y}}{\overrightarrow{u}\cdot\overrightarrow{u}}\overrightarrow{u}$$
- Very cool, but last class we started to generalize this such that we might be able to find an orthogonal projection onto anything.
- Could we find a projection of an $\mathbb{R}^3$ vector onto an $\mathbb{R}^2$ subspace?
- We can do this with an $\mathbb{R}^2$ vector onto a line, which is a subspace of $\mathbb{R}$, so why not?
- **<u>Generalization:</u>**
	- Let $W$ be a subspace of $\mathbb{R}^n$, and let $\left\{\overrightarrow{u}_1,...,\overrightarrow{u}_p\right\}$ be an orthogonal basis of $W$. The <u>orthogonal projection</u> of $\overrightarrow{v}$ onto $W$ is given by: $$\text{proj}_W\left(\overrightarrow{v}\right)=\frac{\overrightarrow{v}\cdot\overrightarrow{u}_1}{\overrightarrow{u}_1\cdot\overrightarrow{u}_1}\overrightarrow{u}_1+...+\frac{\overrightarrow{v}\cdot\overrightarrow{u}_p}{\overrightarrow{u}_p\cdot\overrightarrow{u}_p}\overrightarrow{u}_p$$
	- From this, $\overrightarrow{v}=\overrightarrow{v}_W+\overrightarrow{z}$, and $\overrightarrow{z}\perp W$.
- **<u>Best Approximation Theorem:</u>**
	- Let $W$ be a subspace of $\mathbb{R}^n$, and let $\overrightarrow{v}\in\mathbb{R}^n$. Then $\overrightarrow{v}_W=\text{proj}_W\left(\overrightarrow{v}\right)$ is the nearest point in $W$ to $\overrightarrow{v}$.
	- In other words, $\forall\overrightarrow{w}\in W$: $$||\overrightarrow{v}-\overrightarrow{v}_W||\le ||\overrightarrow{v}-\overrightarrow{w}||$$
	- And this is an equality if and only if $\overrightarrow{w}=\overrightarrow{v}_W$ (duh).
- **<u>Application:</u>**
	- We can use this to calculate the distance from a point to a subspace.
	- It's just $||\overrightarrow{z}||$.
- Why must I be cursed with being a linear algebro?
- **<u>Example:</u>**
	- Calculate the distance from $\overrightarrow{v}$ to $W=\text{Span}\left\{\overrightarrow{u}_1,\overrightarrow{u}_2\right\}$.
	- Well first, we just need an orthogonal basis of $W$, let's represent it as: $\left\{\overrightarrow{w}_1,\overrightarrow{w}_2\right\}$
	- We just want: $$\left|\left|\overrightarrow{v}-\frac{\overrightarrow{v}\cdot\overrightarrow{w}_1}{\overrightarrow{w}_1\cdot\overrightarrow{w}_1}\overrightarrow{w}_1-\frac{\overrightarrow{v}\cdot\overrightarrow{w}_2}{\overrightarrow{w}_2\cdot\overrightarrow{w}_2}\overrightarrow{w}_2\right|\right|$$
	- Easy.
- So the next question is this:
	- What if you don't have an orthogonal basis for $W$?
- Well find one, silly billy.
- You did this in your homework. It was pretty easy.
- **<u>Gram Schmidt Process:</u>**
	- Given $W=\left\{\overrightarrow{v}_1,...,\overrightarrow{v}_p\right\}$, find an orthogonal basis of $W$.
	- The orthogonal basis is shown as $\left\{\overrightarrow{u}_1,...,\overrightarrow{u}_p\right\}$, where: $$\overrightarrow{u_1}=\overrightarrow{v}_1$$ $$\overrightarrow{u}_2=\overrightarrow{v}_2-\text{proj}_{\overrightarrow{u}_1}\left(\overrightarrow{v}_2\right)$$ $$\overrightarrow{u}_3=\overrightarrow{v}_3-\text{proj}_{\overrightarrow{u}_1}\left(\overrightarrow{v}_3\right)-\text{proj}_{\overrightarrow{u}_2}\left(\overrightarrow{v}_3\right)$$ $$\overrightarrow{u}_4=\overrightarrow{v}_4-\text{proj}_{\overrightarrow{u}_1}\left(\overrightarrow{v}_4\right)-\text{proj}_{\overrightarrow{u}_2}\left(\overrightarrow{v}_4\right)-\text{proj}_{\overrightarrow{u}_3}\left(\overrightarrow{v}_4\right)$$ $$...$$

### Orthogonal matrices
- **<u>Example:</u>**
	- So we can just start with a matrix that has orthonormal columns: $$U=\begin{bmatrix}\overrightarrow{u}_1&\overrightarrow{u}_2&\overrightarrow{u}_3\end{bmatrix}$$
	- Let's calculate $U^TU$: $$\begin{bmatrix}\overrightarrow{u}_1^T\\\overrightarrow{u}_2^T\\\overrightarrow{u}_3^T\end{bmatrix}\begin{bmatrix}\overrightarrow{u}_1&\overrightarrow{u}_2&\overrightarrow{u}_3\end{bmatrix}=\begin{bmatrix}\overrightarrow{u}_1\cdot\overrightarrow{u}_1&\overrightarrow{u}_1\cdot\overrightarrow{u}_2&\overrightarrow{u}_2\cdot\overrightarrow{u}_3\\\overrightarrow{u}_2\cdot\overrightarrow{u}_1 & \overrightarrow{u}_2\cdot\overrightarrow{u}_2 & \overrightarrow{u}_2\cdot\overrightarrow{u}_3\\\overrightarrow{u}_3\cdot\overrightarrow{u}_1&\overrightarrow{u}_3\cdot\overrightarrow{u}_2&\overrightarrow{u}_3\cdot\overrightarrow{u}_3\end{bmatrix}$$
	- Because these are orthonormal columns, we simplify to: $$\begin{bmatrix}1 & 0 & 0\\0 & 1 & 0\\0 & 0 & 1\end{bmatrix}$$
- **<u>Theorem:</u>**
	- An $m\text{x}n$ matrix, $A$, has orthonormal columns if and only if $A^TA=I$. In this case:
		1. $\left|\left|A\overrightarrow{x}\right|\right|=\left|\left|\overrightarrow{x}\right|\right|$
		2. $\left(A\overrightarrow{x}\ \right)\cdot\left(A\overrightarrow{y}\ \right)=\overrightarrow{x}\cdot\overrightarrow{y}$
- **<u>Theorem:</u>**
	- If $A$ is an $n\text{x}n$ matrix with orthonormal columns, then $A$ is invertible and $A^{-1}=A^T$.
	- Matrices with this property are called <u>orthogonal matrices</u>.
- **<u>Spectral Theorem:</u>**
	- If $A$ is an $n\text{x}n$ matrix such taht $A^T=A$, then:
		1. $A$ is diagonalizable ($A=PDP^{-1}$).
		2. $P$ can be chosen  to have orthonormal columns ($P^{-1}=P^T$).
	- We won't be tested on this necessarily, but we might be able to use it on the test.
	- Certainly very cool.