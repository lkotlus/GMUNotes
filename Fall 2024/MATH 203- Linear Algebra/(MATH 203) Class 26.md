### Last class!
- Basic grading changes, see previous class.
- Today should just be review.
- Final exam:
	- On Tuesday, December 17.
	- Goes from 4:30-7:15 PM.
	- Normal class location.

### Diagonalization
- We have a matrix, $A$, and we want to write it as $PDP^{-1}$.
- Get your eigenvalues $\left\{\lambda_1,...,\lambda_n\right\}$, and $D$ is: $$D=\begin{bmatrix}\lambda_1&...&0\\&...&\\0&...&\lambda_n\end{bmatrix}$$
- With the corresponding set of eigenvectors $\left\{\overrightarrow{v}_1,...,\overrightarrow{v}_n\right\}$, such that $\overrightarrow{v}_k$ is the eigenvector for $\lambda_k$, $P$ is: $$P=\begin{bmatrix}\overrightarrow{v}_1&...&\overrightarrow{v}_n\end{bmatrix}$$
- This is dependent upon the eigenvectors forming a basis of $\mathbb{R}^n$. Also recall that our eigenvalues will repeat depending on their multiplicity.
- **<u>How to find it:</u>**
	1. Find the eigenvalues of $A$ by solving the characteristic equation: $$\text{det}\left(A-\lambda I\right)=0$$
	2. Now we want our eigenvectors! For each $\lambda$, solve: $$(A-\lambda I)\overrightarrow{x}=\overrightarrow{0}$$
	3. If all of the eigenvectors from step 2 give a basis of $\mathbb{R}^n$, we are ready to go and the matrix is diagonalizable.
- **<u>About diagonalizability:</u>**
	- When fully factored, our characteristic equation might look something like: $$\lambda^5(\lambda-4)^2(\lambda+2)^3=0$$
	- This corresponds to a $10\text{x}10$ matrix, which we can find from the sum of our multiplicities.

#### Review Problem 1
- Consider the following matrix: $$B=\begin{bmatrix}-1&-1&-2\\-1&0&-1\\1&1&2\end{bmatrix}$$
- Show that $B$ is not diagonalizable.
- **<u>Solution:</u>**
	- We don't have enough eigenvectors!

#### Review Problem 2
- Let: $$\overrightarrow{w}_1=\begin{bmatrix}1\\1\\-1\end{bmatrix},\ \  \overrightarrow{w}=\begin{bmatrix}1\\0\\0\end{bmatrix}, \ \ W=\text{Span}\left\{\overrightarrow{w}_1,\ \overrightarrow{w}_2\right\}$$ $$\overrightarrow{v}=\begin{bmatrix}1\\1\\1\end{bmatrix}$$
- Please:
	1. Use the Gram-Schmidt process to find an orthogonal basis $\left\{\overrightarrow{v}_1,\ \overrightarrow{v}_2\right\}$ of $W$ with $\overrightarrow{v}_1=\overrightarrow{w}_1$.
	2. Calculate the orthogonal projection of $\overrightarrow{v}$ onto $W$.
	3. Find the distance from $\overrightarrow{v}$ to $W$.
- **<u>Solution:</u>**
	1. Gram-Schmidt:
		- So just use the exact formula to get: $$\overrightarrow{v}_2=\overrightarrow{w}_2-\text{proj}_{\overrightarrow{v}_1}\left(\overrightarrow{w}_2\right)$$
	2. Orthogonal projection:
		- Just use the formula, again: $$\text{proj}_W\left(\overrightarrow{v}\right)=\frac{\overrightarrow{v}_1\cdot\overrightarrow{v}}{\overrightarrow{v}_1\cdot\overrightarrow{v}_1}\overrightarrow{v}_1+\frac{\overrightarrow{v}_2\cdot\overrightarrow{v}}{\overrightarrow{v}_2\cdot\overrightarrow{v}_2}\overrightarrow{v}_2$$
	3. Distance:
		- Take the orthogonal projection $\overrightarrow{v}_W$ and calculate $\overrightarrow{z}=\overrightarrow{v}-\overrightarrow{v}_W$. Finally, just get: $$\left|\left|\ \overrightarrow{z}\ \right|\right|$$
		- Magnitude of $\overrightarrow{z}$ is our distance, seeing as $\overrightarrow{z}$ is the most direct path from $W$ to $\overrightarrow{v}$.

#### Review Problem 3
- Let $A$ be a $9\text{x}10$ matrix:
	- What is the maximum possible dimension of the column space of $A$?
		- Solution: 9
	- What is the minimum possible dimension of the nullspace of $A$?
		- Solution: 1
	- Suppose that in addition you happen to know that the rows of $A$ are linearly dependent. How can you sharpen/strengthen your answers to the first two questions?
		- Solution: values would go to 8 and 2.