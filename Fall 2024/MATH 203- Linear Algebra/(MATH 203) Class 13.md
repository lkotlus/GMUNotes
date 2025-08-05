### Properties of determinants
- To calculate a determinant using row reduction:
	- The determinant doesn't change if you add a multiple of a row to another.
	- The determinant flips sign if you swap two rows.
	- The determinant is multiplied by $\frac{1}{c}$ if you multiply a row by $c$.
- **<u>Comments:</u>**
	- If $A$ is an $n\text{x}n$ matrix and $c\in\mathbb{R}$, then: $$\text{det}(cA)=|cA|=c^n|A|$$
	- Let $A=\begin{bmatrix}\overrightarrow{a}_1 & \overrightarrow{a}_2\end{bmatrix}$, and suppose that $\overrightarrow{a}_1, \overrightarrow{a}_2\in\mathbb{R}^2$. Consider $\text{T}\left(\overrightarrow{x}\right)=A\overrightarrow{x}$, it follows that $\text{T}\left(\overrightarrow{e}_1\right)=\overrightarrow{a}_1$, $\text{T}\left(\overrightarrow{e}_2\right)=\overrightarrow{a}_2$. From this, we can figure out that the area of the parallelogram formed by $\overrightarrow{a}_1$ and $\overrightarrow{a}_2$ is equal to $|\text{det}(A)|$ (absolute value of the determinant).
		- Abridged: area in the shape formed by $\overrightarrow{a}_1, \overrightarrow{a}_2$ is equal to $\left|\text{det}\left(\begin{bmatrix}\overrightarrow{a}_1 & \overrightarrow{a}_2\end{bmatrix}\right)\right|$
		- More than that, the sign tells us clockwise vs. counterclockwise.
		- We can even apply this to higher dimensions!
- **<u>Theorems:</u>**
	- $\text{det}(A)\ne 0\iff A$ is invertible
	- $\text{det}(A)=\text{det}(A^T)$
	- $\text{det}(AB)=\text{det}(A)\,\,\text{det}(B)$
- **<u>Comments:</u>**
	- $\text{det}(A+B)\ne \text{det}(A)+\text{det}(B)$
	- There are explicit formulas (Cramer's rule) for solutions of systems of equations in terms of determinants.
	- It is possible to give an explicit formula for the inverse of an $n\text{x}n$ matrix involving determinants (not really useful beyond $2\text{x}2$).

### Vector spaces and subspaces
- This is a very abstract section.
- **<u>Definition:</u>**
	- A *vector space* is a non-empty set $V$ of objects called *vectors* on which are defined two operations called *addition* and *scalar multiplication*, satisfying the following axioms $\forall\overrightarrow{u}, \overrightarrow{v},\overrightarrow{w}\in V$ and $\forall c, d\in\mathbb{R}$. 
		1. The sum of $\overrightarrow{u}, \overrightarrow{v}$ is in $V$, denoted $\overrightarrow{u}+\overrightarrow{v}\in V$
		2. $\overrightarrow{u}+\overrightarrow{v}=\overrightarrow{v}+\overrightarrow{u}$
		3. $(\overrightarrow{u}+\overrightarrow{v})+\overrightarrow{w}=\overrightarrow{u}+(\overrightarrow{v}+\overrightarrow{w})$
		4. There is a zero vector in $V$ $|$ $\overrightarrow{v}+\overrightarrow{0}=\overrightarrow{v}$
		5. $\forall\overrightarrow{u}$ there is a vector $-\overrightarrow{u}$ $|$ $\overrightarrow{u}-\overrightarrow{u}=\overrightarrow{0}$
		6. The scalar multiplication of $\overrightarrow{u}$ and $c$ is in $V$, denoted $c\overrightarrow{u}\in V$
		7. $c(\overrightarrow{u}+\overrightarrow{v})=c\overrightarrow{u}+c\overrightarrow{v}$
		8. $(c+d)\overrightarrow{u}=c\overrightarrow{u}+d\overrightarrow{u}$
		9. $c(d\overrightarrow{u})=(cd)\overrightarrow{u}$
		10. $1\cdot\overrightarrow{u}=\overrightarrow{u}$
- **<u>Example:</u>**
	- $V=\mathbb{R}^n$, usual vector addition and scalar multiplication.
- **<u>Example:</u>**
	- $V=\mathbb{P}_n=\{\text{Polynomials of degree at most n}\}=\{a_0+a_1t+a_2t^2+...+a_nt^n\ |\ a_0, a_1, ..., a_n \in\mathbb{R}\}$
	- This is a vector space...
	- So here, a vector is a polynomial of degree $n$.
	- The zero polynomial is $a_0+a_1t+a_2t^2+...+a_nt^n\ |\ a_0, a_1, ..., a_n=0$.
	- We can see that all of our axioms hold true.
- **<u>Example:</u>**
	- $V=\mathbb{P}=\{\text{all polynomials}\}$
- **<u>Example:</u>**
	- $V=\mathbb{R}^{\infty}=\left\{\begin{bmatrix}u_1\\u_2\\u_3\\...\end{bmatrix}\ |\ u_1, u_2, ...\in\mathbb{R}\right\}$
- **<u>Example:</u>**
	- $S$ is any set.
	- $V=\text{set of functions}\ f:S\rightarrow\mathbb{R}$
	- This works because our vectors are just functions, and functions hold these properties!
- **<u>Definition:</u>**
	- A subspace of $V$ is a subset $H$ of $V$ such that:
		1. $\overrightarrow{0}\in H$
		2. $H$ is closed under vector addition
			- This means that $\overrightarrow{u},\overrightarrow{v}\in H\iff\overrightarrow{u}+\overrightarrow{v}\in H$
		3. $H$ is closed under scalar multiplication
			- This means that for $c\in\mathbb{R}$, $\overrightarrow{u}\in H\iff c\overrightarrow{u}\in H$