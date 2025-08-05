### Dimensions of Vector Spaces
- **<u>Theorem:</u>**
	- Let $V$ be a vector space with basis $B=\left\{\overrightarrow{b}_1,...\overrightarrow{b}_n\right\}$.
	- Given the above,
		1. Any set of more than $n$ vectors is LD.
		2. Any set of less than $n$ vectors does not span $V$.
		3. Any other basis of $V$ has exactly $n$ vectors.
- We hold these truths to be self-evident, however it is being discussed ad nauseam. 
- **<u>Definition:</u>**
	- Let $V$ be a vector space. If $V$ has a finite basis, then $V$ is set to be <u>finite-dimensional</u>. 
	- Should the length of the basis be $n$, then we call $V$ $n$-dimensional. This is calculated as $\text{dim}\ V$.
	- If $V$ does not have a finite basis, then $V$ is said to be <u>infinite dimensional</u>.
- **<u>Example:</u>**
	- $\mathbb{R}^n$ is $n$-dimensional (the standard bases $\left\{\overrightarrow{e}_1,...,\overrightarrow{e}_n\right\}$ has $n$ vectors).
- **<u>Example:</u>**
	- $\mathbb{P}_n=\left\{a_0+a_1t+a_2t^2+...+a_nt^n\ |\ a_0,...,a_n\in\mathbb{R}\right\}$.
	- The basis of this would be $\left\{1,t,t^2,...,t^n\right\}$, therefore $\text{dim}\ \mathbb{P}_n=n+1$.
- **<u>Example:</u>**
	- $H=\text{Span}\left\{\begin{bmatrix}1\\2\\1\end{bmatrix},\begin{bmatrix}-2\\1\\0\end{bmatrix}\right\}$
	- $\text{dim}\ H=2$.
- **<u>Example:</u>**
	- The following set is a vector subspace of of $\mathbb{R}^4$, find it's dimension: $$H=\left\{\begin{bmatrix}a+2b-c\\2a+2b\\-b+c\\-a-c\end{bmatrix}\ |\ a,b,c\in\mathbb{R}\right\}$$
	- Well, first let's split out that given vector to see the following: $$H=\text{Span}\left\{\begin{bmatrix}1\\2\\0\\-1\end{bmatrix}, \begin{bmatrix}2\\2\\-1\\0\end{bmatrix}, \begin{bmatrix}-1\\0\\1\\-1\end{bmatrix}\right\}$$
	- Well we need to find a basis for $H$, which would just be the column space of a matrix formed by the vectors in the span. Let's row reduce to get: $$A=\begin{bmatrix}1&2&-1\\2&2&0\\0&-1&1\\-1&0&-1\end{bmatrix}$$ $$\begin{bmatrix}1&2&-1\\0&1&-1\\0&0&0\\0&0&0\end{bmatrix}$$
	- This gives us the column space: $$\text{Col}\ A=\left\{\begin{bmatrix}1\\2\\0\\-1\end{bmatrix},\begin{bmatrix}2\\2\\-1\\0\end{bmatrix}\right\}$$
	- From that, we know that $\left\{\begin{bmatrix}1\\2\\0\\-1\end{bmatrix},\begin{bmatrix}2\\2\\-1\\0\end{bmatrix}\right\}$ is a basis for $H$, so $\text{dim}\ H=2$.
- **<u>Example:</u>**
	- Describe all subspaces of $\mathbb{R}^3$ by dimension.
		- 0-dimensional subspace: $\left\{\overrightarrow{0}\right\}$
		- 1-dimensional subspaces: lines through the origin
		- 2-dimensional subspaces: planes through the origin
		- 3-dimensional subspaces: $\mathbb{R}^3$
	- 0-dimensional and 3-dimensional are unique!
- **<u>Theorem:</u>**
	- Let $V$ be a finite-dimensional vector space. 
	- Then, 
		1. Any LI subset of $V$ can be expanded to a basis.
		2. Any set of vectors that spans $V$ can be shrunk to a basis.
- **<u>Theorem:</u>**
	- Let $H$ be a subspace of a finite-dimensional vector space, $V$.
	- Then, $\text{dim}\ H\le\text{dim}\ V$.
- **<u>Theorem:</u>**
	- Let $V$ be an $n$-dimensional vector space.
	- Then, 
		1. Any set of $n$ LI vectors is automatically a basis.
		2. Any set of $n$ vectors that spans $V$ is automatically a basis.
- Recall that if $A$ is an $m\text{x}n$ matrix, then we defined 3 subspaces associated to it:
	1. $\text{Nul}\ A$ ($\left\{\overrightarrow{v}\ |\ A\overrightarrow{v}=\overrightarrow{0}\right\}$)
	2. $\text{Col}\ A$ (span of the columns of $A$)
	3. $\text{Row}\ A$ (span of the rows of $A$)
- We can get the dimensions of these as well:
	- $\text{dim Col}\ A=\text{\# pivots in }RREF(A)=\text{dim Row}\ A$.
		- This is called the <u>rank</u> of $A$
	- $\text{dim Nul}\ A$ is called the <u>nullity</u> of $A$.
- **<u>Rank theorem:</u>**
	- For any matrix, $A$: $\text{rank}\ A+\text{nullity}\ A=\text{\# columns of }A$.
	- If $A$ is an $m\text{x}n$ matrix, then $\text{rank }A+\text{nullity }A=n$.
	- From this, we know that $\text{nullity }A=\text{\# non-pivot columns of }A$.
	- Number of pivot columns and the number of non-pivot columns is, quite obviously, the number of columns.
- **<u>Example:</u>**
	- **<u>"These are the big guns, the linear algebra wizardry to impress your friends at the park."</u>**
	- If $A$ is $8\text{x}11$ and $\text{dim Nul }A=3$, what is the what is $\text{dim Col }A$?
	- Well, $11-3=8$, so $\text{dim Col }A=8$
- **<u>Example:</u>**
	- Can a $5\text{x}10$ matrix have a nullity of 4?
	- No! That means the rank would need to be 6, implying 6 pivot positions. But we can't have 6 pivot positions, because there's only 5 rows!
	- Legit. This would impress my friends at the park.
- **<u>Example:</u>**
	- Suppose you have 18 linear equations in 20 variables ($18\text{x}20$ matrix).
		- $A\overrightarrow{x}=\overrightarrow{b}$
	- You solve and find it's consistent, and the general solution has 2 free variables.
	- If someone gave you a different vector, $\overrightarrow{c}$, as the solution could you guarantee that it will still be consistent?
	- Yes!
	- You have 18 linearly independent columns ($20-2=18$), so that means you span the entire vector-space for your solutions ($\mathbb{R}^{18}$). 
	- That means every vector is in the column space!
- **<u>Invertible matrix theorem (extended):</u>**
	1. $A$ is invertible.
	2. $A$ can be row reduced to $I_n$.
	3. $A\overrightarrow{x}=\overrightarrow{0}$ has only the trivial solution.
	4. The columns of $A$ are LI.
	5. $\text{T}\left(\overrightarrow{x}\right)=A\overrightarrow{x}$ is one-one.
	6. $A\overrightarrow{x}=\overrightarrow{b}$ has at least one solution $\forall\overrightarrow{b}$.
	7. Columns of $A$ span $\mathbb{R}^n$.
	8. $\text{T}\left(\overrightarrow{x}\right)=A\overrightarrow{x}$ is onto.
	9. There exists a square matrix $C$ $|$ $CA=I_n$.
	10. There exists a square matrix $D$ $|$ $AD=I_n$.
	11. $A^T$ is invertible.
	12. $\text{det}(A)\ne0$
	13. $\text{Col }A=\mathbb{R}^n$
	14. $\text{Row }A=\mathbb{R}^n$
	15. ... (more stuff, all logicable)
- "It's like the Jedi Knights"