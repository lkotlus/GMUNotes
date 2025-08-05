### Eigenmath
- Diagonalization!
	- Many use cases, but if we wan't to find $A^n$ we would use this (as an example).
- **<u>Example:</u>**
	- $D=\begin{bmatrix}2 & 0\\0 & -3\end{bmatrix}$. Compute $D^{100}$.
	- For a normal $2\text{x}2$ matrix, this is hard. But because this is a diagonal matrix we know it's just equal to $\begin{bmatrix}a^n & 0\\0 & b^n\end{bmatrix}$.
	- Pretty neat, so for this we have $D^{100}=\begin{bmatrix}2^{100} & 0\\0 & (-3)^{100}\end{bmatrix}$
- But what if we don't have a diagonal matrix?
- **<u>Example:</u>**
	- $A=\begin{bmatrix}7 & 2\\-4 & 1\end{bmatrix}$. Well, $A$ is actually similar to another matrix (which happens to be diagonal), $D=\begin{bmatrix}5 & 0\\0 & 3\end{bmatrix}$, with $P=\begin{bmatrix}1 & 1\\-1 & -2\end{bmatrix}$ such that $A=PDP^{-1}$. 
	- Well, $A^2=(PDP^{-1})(PDP^{-1})=PDP^{-1}PDP^{-1}=PDDP^{-1}=PD^2P^{-1}$
	- This pattern continues because our inverses always multiply with the normal ones to give $I$! This means we know that $A^k=PD^kP^{-1}$. That's pretty easy to compute, especially if we need to calculate with a high value of $k$.
- **<u>Definition:</u>**
	- A square matrix, $A$, is called <u>diagonalizable</u> if $A$ is similar to a diagonal matrix, i.e. there is an invertible matrix, $P$, and diagonal matrix, $D$, such that $A=PDP^{-1}$.
	- Neat, but how do I find it?!
- **<u>Diagonalization Theorem:</u>**
	- An $n\text{x}n$ matrix, $A$, is diagonalizable $\iff$ $A$ has $n$ linearly independent eigenvectors.
	- In this case, the columns of $P$ are the eigenvectors, and the diagonal entries of $D$ are corresponding eigenvalues.
	- THIS IS REALLY COOL!!!
	- In other words, if $\overrightarrow{v}_1,...,\overrightarrow{v}_n$ are linearly independent eigenvectors with corresponding eigenvalues $\lambda_1,...,\lambda_n$, then $P=\left[\overrightarrow{v}_1 \ \ ... \ \ \overrightarrow{v}_n\right]$ and $D=\begin{bmatrix}\lambda_1 & ... & 0\\&...\\0 & ... & \lambda_n\end{bmatrix}$
	- Note:
		- $P$ and $D$ are not necessarily unique!
		- We will <u>never</u> have more than $n$ eigenvalues because the characteristic equation has a degree of $n$, which gives only $n$ possible solutions!
- **<u>Example:</u>**
	- Diagonalize $A=\begin{bmatrix}1 & 3 & 3\\-3 & -5 & -3\\3 & 3 & 1\end{bmatrix}$ (if possible).
	- Well, first let's find the eigenvalues:
		- $\text{det}(A-\lambda I)=0$
		- This gives us $-(\lambda -1)(\lambda + 2)^2$
		```functionplot
		y=-(x -1)(x + 2)^2
		```
		- This gives $\lambda=1$ (multiplicity 1) or $\lambda=-2$ (multiplicity 2).
	- So the next step is to find a basis for each eigenspace.
		- For $\lambda=1$:
			- Solve $(A-\lambda I)\overrightarrow{x}=\overrightarrow{0}$
			- ...
			- General solution is $\overrightarrow{x}=x_3\begin{bmatrix}1\\-1\\1\end{bmatrix}$
			- So a basis of this eigenspace is $\left\{\begin{bmatrix}1\\-1\\1\end{bmatrix}\right\}$.
		- For $\lambda=-2$:
			- Same process.
			- ...
			- General solution is $\overrightarrow{x}=x_2\begin{bmatrix}-1\\1\\0\end{bmatrix}+x_3\begin{bmatrix}-1\\0\\1\end{bmatrix}$
			- So a basis of this eigenspace is $\left\{\begin{bmatrix}-1\\1\\0\end{bmatrix},\begin{bmatrix}-1\\0\\1\end{bmatrix}\right\}$.
	- Well, we have a $3\text{x}3$ matrix and 3 linearly independent vectors. So we're ready to go! Let's plug in values for $P$ and $D$: $$P=\begin{bmatrix}1 & -1 & -1\\-1 & 1 & 0\\1 & 0 & 1\end{bmatrix}$$ $$D=\begin{bmatrix}1 & 0 & 0\\0 & -2 & 0\\0 & 0 & -2\end{bmatrix}$$
	- Very nice. Note that we needn't check if vectors from different eigenspaces are linearly indpendent, as they are by definition.
	- We could double check if we've done things correctly by calculating $A=PDP^{-1}$.
- **<u>Example:</u>**
	- Diagonalize $A=\begin{bmatrix}2 & 1\\0 & 2\end{bmatrix}$ (if possible).
	- Find determinant:
		- $\text{det}(A-\lambda I)=0$
		- $(2-\lambda)^2=0$
		- $\lambda=2$ (just one with multiplicity 2)
		```functionplot
		y=(2-x)^2
		```
	- So now we solve $(A-2I)\overrightarrow{x}=\overrightarrow{0}$:
		- General solution is: $\overrightarrow{x}=x_1\begin{bmatrix}1\\0\end{bmatrix}$.
		- So our basis is $\left\{\begin{bmatrix}1\\0\end{bmatrix}\right\}$.
	- **<u>"We failed! We failed."</u>**
	- Since there is only one linearly independent eigenvector, we can conclude that $A$ is not diagonalizable.
- **<u>Theorem:</u>**
	- If $\left\{\overrightarrow{v}_1,...,\overrightarrow{v}_2\right\}$ are eigenvectors of $A$ that correspond to <u>distinct</u> eigenvalues $\lambda_1,...,\lambda_n$, then $\left\{\overrightarrow{v}_1,...,\overrightarrow{v}_n\right\}$ is a linearly independent set.
- **<u>Example:</u>**
	- Diagonalize $A=\begin{bmatrix}4 & 3 & -2\\0 & 1 & 3\\0 & 0 & -1\end{bmatrix}$ if possible.
	- Well, it's upper diagonal, so $\lambda_1,\lambda_2,\lambda_3=4,1,-1$.
	- Mindless work...
	- ...
- **<u>Theorem:</u>**
	- Let $A$ be an $n\text{x}n$ matrix whose distinct eigenvalues are $\lambda_1,...,\lambda_p$.
	- Then:
		1. The dimension of the $\lambda_k$ eigenspace is less than or equal to the multiplicity of $\lambda_k$.
		2. $A$ is diagonalizable $\iff$ the sum of the dimensions of the eigenspaces is equal to $n$. This happens if and only if 
			- The characteristic polynomial factors completely into linear factors.
			- Dimension of the $\lambda_k$ eigenspace must be equal to the multiplicity of $\lambda_k$ $\forall k$.
		3. If $A$ is diagonalizable, and $\mathcal{B}_k$ is a basis for the $\lambda_k$ eigenspace, then the total collection of vectors in $\mathcal{B}_1, ..., \mathcal{B}_p$ is a basis of eigenvectors of $\mathbb{R}^n$.