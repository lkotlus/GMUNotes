### FIRE FIRE FIRE
- We had to delay for a fire drill :(

### Dot product, length, orthogonality
- **<u>Definition:</u>**
	- Let $\overrightarrow{u}=\begin{bmatrix}u_1\\...\\u_n\end{bmatrix}$ and $\overrightarrow{v}=\begin{bmatrix}v_1\\...\\v_n\end{bmatrix}$ be vectors in $\mathbb{R}^n$.
	- The <u>dot product</u> (<u>or inner product</u>, or <u>scalar product</u>) of $\overrightarrow{u}$ and $\overrightarrow{v}$ is: $$\overrightarrow{u}\cdot\overrightarrow{v}=\overrightarrow{u}^T\overrightarrow{v}=u_1v_1+...+u_nv_n=\sum_{k=0}^nu_kv_k$$
- **<u>Theorem:</u>**
	1. $\overrightarrow{v}\cdot\overrightarrow{u}=\overrightarrow{v}\cdot\overrightarrow{u}$
	2. $(\overrightarrow{u}+\overrightarrow{v})\cdot\overrightarrow{w}=\overrightarrow{u}\cdot\overrightarrow{w}+\overrightarrow{v}\cdot\overrightarrow{w}$
	3. $(c\overrightarrow{u})\cdot\overrightarrow{v}=c(\overrightarrow{u}\cdot\overrightarrow{v})$
	4. $\overrightarrow{u}\cdot\overrightarrow{u}\ge 0\land\overrightarrow{u}\cdot\overrightarrow{u}=0\iff\overrightarrow{u}=\overrightarrow{0}$
- **<u>Definition:</u>**
	- The <u>length</u> (or <u>norm</u>) of a vector $\overrightarrow{v}$ is: $$||\overrightarrow{v}||=\sqrt{\overrightarrow{v}\cdot\overrightarrow{v}}$$
	- If $\overrightarrow{v}=\begin{bmatrix}v_1\\...\\v_n\end{bmatrix}$, then $||\overrightarrow{v}||=\sqrt{v_1^2+...+v_2^2}$
	- Note that $||c\overrightarrow{v}||=|c|\ ||\overrightarrow{v}||$.
- **<u>Definition:</u>**
	- Any vector $\overrightarrow{v}$ with length 1 is called a <u>unit vector</u>. Any non-zero vector can be re-scaled to have length 1:
	- Well, the length of $\overrightarrow{v}$ is $\sqrt{\overrightarrow{v}\cdot\overrightarrow{v}}$. We could divide by it to turn our vector into a unit vector. That would be $\overrightarrow{u}=\frac{\overrightarrow{v}}{||\overrightarrow{v}||}$.
	- That is, $\overrightarrow{u}$ points in the same direction as $\overrightarrow{v}$, but has a length of 1.
- **<u>The talk:</u>**
	- Well, recall that vectors are just arrows in $\mathbb{R}^n$ when we make pictures of them.
	- If we make a lil' triangle with two vectors at the origin and one connecting the two, then that connector is the difference between the base vectors.
	- The <u>distance</u> between two vectors is given by $\text{dist}(\overrightarrow{u},\overrightarrow{v})=||\overrightarrow{u}-\overrightarrow{v}||$.
	- Notice that $\text{dist}(\overrightarrow{u},\overrightarrow{v})^2=||(\overrightarrow{u}-\overrightarrow{v})||^2=(\overrightarrow{u}-\overrightarrow{v})\cdot (\overrightarrow{u}-\overrightarrow{v})$.
	- We can distribute, which gives $\overrightarrow{u}\cdot\overrightarrow{u}-\overrightarrow{u}\cdot\overrightarrow{v}-\overrightarrow{v}\cdot\overrightarrow{u}+\overrightarrow{v}\cdot\overrightarrow{v}$
	- If you think hard, this gives us: $||\overrightarrow{u}||^2-2\overrightarrow{u}\cdot\overrightarrow{v}+||\overrightarrow{v}||^2$
	- So that's the length of this triangle? Well, this is the same as the law of cosines! $a^2+b^2-2ab\cos(\theta)$ is the same thing as $||\overrightarrow{u}||^2+||\overrightarrow{v}||^2-2\overrightarrow{u}\cdot\overrightarrow{v}$. 
	- This is also secretly a proof that $\overrightarrow{u}\cdot\overrightarrow{v}=||\overrightarrow{u}||\ ||\overrightarrow{v}||\cos(\theta)$.
- **<u>Definition:</u>**
	- Vectors $\overrightarrow{u},\overrightarrow{v}$ are called <u>orthogonal</u> if $\overrightarrow{u}\cdot\overrightarrow{v}$ (assuming both are nonzero).
- **<u>Theorem:</u>**
	- If $\overrightarrow{u}$ and $\overrightarrow{v}$ are orthogonal, then $||\overrightarrow{u}\pm\overrightarrow{v}||=||\overrightarrow{u}||^2+||\overrightarrow{v}||^2.$
- **<u>Planes and whatnot:</u>**
	- Recall that $3x_1-2x_2+x_3=0$ represents a 2-dimensional subspace of $\mathbb{R}^3$. 
	- We could write this as a matrix times a vector, more specifically: $$\begin{bmatrix}3 & -2 & 1\end{bmatrix}\begin{bmatrix}x_1\\x_2\\x_3\end{bmatrix}=\overrightarrow{0}$$
	- Well this looks like a dot product, let's rewrite it: $$\begin{bmatrix}3\\-2\\1\end{bmatrix}\cdot\begin{bmatrix}x_1\\x_2\\x_3\end{bmatrix}=0$$
	- Well this is just the set of all vectors orthogonal to $\begin{bmatrix}3\\-2\\1\end{bmatrix}$.
	- Pretty cool!
	- Well, let's re-frame this.
	- We have a 2-dimensional subspace $P=\left\{\overrightarrow{x}\in\mathbb{R}^n\ |\begin{bmatrix}3\\-2\\1\end{bmatrix}\cdot\overrightarrow{x}=0\right\}$
	- We have a 1-dimensional subspace $L=\text{Span}\left\{\begin{bmatrix}3\\-2\\1\end{bmatrix}\right\}$.
	- We call $P$ the <u>orthogonal complement</u> to $L$, notation is $P=L^\perp$.
	- In this case, $L$ is also the set of all vectors orthogonal to $P$. $P$ is our plane, $L$ is just every vector that could be the vector used to define it. Easy.
- **<u>Definition:</u>**
	- Let $W$ be a subspace of $\mathbb{R}^n$.
	- The set of vectors orthogonal to every vector in $W$ is a subspace of $\mathbb{R}^n$ denoted $W^\perp$, called the <u>orthogonal complement</u> of $W$: $$W^\perp=\left\{\overrightarrow{x}\in\mathbb{R}^n\ |\ \overrightarrow{w}\cdot\overrightarrow{x}=0\ \forall\overrightarrow{w}\in W\right\}$$
- **<u>Example:</u>**
	- Find a basis for the orthogonal complement of $W=\text{Span}\left\{\begin{bmatrix}1\\1\\1\\0\end{bmatrix}\begin{bmatrix}-1\\1\\0\\1\\\end{bmatrix}\right\}$.
	- Well, let's call the vectors in these sets $\overrightarrow{a}_1$ and $\overrightarrow{a}_2$ respectively. Well we know that $W^\perp$ is just every vector that satisfies $\overrightarrow{a}_1\cdot\overrightarrow{x}=0$ and $\overrightarrow{a}_2\cdot\overrightarrow{x}=0$.
	- We also know that those are just $\overrightarrow{a}_1^T\overrightarrow{x}=\overrightarrow{0}$  and $\overrightarrow{a}_2^T\overrightarrow{x}=\overrightarrow{0}$.
	- This is a system of equations! $A\overrightarrow{x}=\overrightarrow{0}$: $$A=\begin{bmatrix}\overrightarrow{a}_1^T\\\overrightarrow{a}_2^T\end{bmatrix}=\begin{bmatrix}1 & 1& 1& 0\\-1& 1 & 0 & 1\end{bmatrix}$$
	- Solve for $\overrightarrow{0}$ to get: $$\overrightarrow{x}=x_3\begin{bmatrix}-\frac{1}{2}\\-\frac{1}{2}\\1\\0\end{bmatrix}+x_4\begin{bmatrix}\frac{1}{2}\\-\frac{1}{2}\\0\\1\end{bmatrix}$$
	- Well, that tells us that the following set is a basis of $W^\perp$: $$\left\{\begin{bmatrix}-\frac{1}{2}\\-\frac{1}{2}\\1\\0\end{bmatrix},\begin{bmatrix}\frac{1}{2}\\-\frac{1}{2}\\0\\1\end{bmatrix}\right\}$$
	- Very cool.
- **<u>Comment:</u>**
	- The dimension of $W$ and the dimension of $W^\perp$ sum to $n$.