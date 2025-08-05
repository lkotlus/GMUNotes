### Determinants!
- We spoke about this briefly for $2\text{x}2$ matrices.
- Let $$A=\begin{bmatrix}a & b\\c & d\end{bmatrix}$$
- We defined the determinant of $A$ to be: $$\text{det}(A)=\begin{vmatrix}a & b \\ c & d\end{vmatrix} = ad-bc$$
- We also saw previously that $A$ is invertible $\iff$ $\text{det}(A)\ne 0$ (for $2\text{x}2$ matrices)
- So let's try to generalize this to work for $n\text{x}n$ matrices.
- Some notation to keep in mind for the following definition:

|Notation|Example|
|---------|--------|
| $A$ is an $n\text{x}n$ matrix.|$A=\begin{bmatrix}1&2&3\\4&5&6\\7&8&9\end{bmatrix}$|
|$a_{ij}$ is the $(i, j)$ entry of $A$|$a_{23}=6$|
| $A_{ij}$ is the $(n-1)\text{x}(n-1)$ matrix resulting from removing the $i$ row and $j$ column from $A$.|$A_{13}=\begin{bmatrix}4&5\\7&8\end{bmatrix}$|

- Very cool!
- **<u>Definition:</u>**
	- The determinant of $A$ is: $$\text{det}(A) = \left|A\right| = a_{11}\text{det}(A_{11})-a_{12}\text{det}(A_{12})+a_{13}\text{det}(A_{13})-...$$ $$\text{det}(A)= \left|A\right| = \sum^n_{j=1}(-1)^{j+1}a_{1j}\text{det}(A_{1j})$$
	- Very cool.
	- This is a recursive definition that goes all the way until we hit $2\text{x}2$ matrices.
- **<u>Definition:</u>**
	- Firstly, $C_{ij}=(-1)^{i+j}|A_{ij}|$ is called the $(i,j)$-cofactor of $A$
	- With this, we can clean up our formula a bit: $$\text{det}(A)= \left|A\right| = \sum^n_{j=1}a_{1j}C_{1j}$$
	- We call that the cofactor expansion of the determinant along row 1.
- **<u>Crazy theorem:</u>**
	- "Conspiracy Theorem"
	- $\text{det}(A)$ can be computed by cofactor expansion along any row or any column.
	- This means that for any $i$: $$\text{det}(A)=|A|=\sum^n_{j=1}a_{ij}C_{ij}$$
	- And for any $j$: $$\text{det}(A)=|A|=\sum^n_{i=1}a_{ij}C_{ij}$$
	- We can pick rows and columns to go *faster*.
- Example:
	- Take the following matrix: $$A=\begin{bmatrix}1&2&-2&1\\3&5&0&7\\1&-2&0&4\\-2&0&0&1\end{bmatrix}$$
	- Well, column 3 looks like it's pretty nice! There's lots of zeroes, so a ton of stuff just cancels.
	- $|A|=-2|A_{13}|-0|A_{23}|+0|A_{33}|-0|A_{34}|$
	- And that just means that $|A|=-2|A_{13}|$. That's just a $3\text{x}3$ matrix, pretty easy!
	- Just to be explicit: $$|A|=-2\begin{vmatrix}3&5&7\\1&-2&4\\-2&0&1\end{vmatrix}$$
	- For $|A_{13}|$, we should choose to go along column 2 or row 3 to use that handy 0.
- If you're an absolute ***<u>SCRUB</u>*** and need help to remember the sign of the thing your on in this process, just use this checkerboard pattern: $$\begin{bmatrix}+&-&+&-&...\\-&+&-&+&...\\+&-&+&-&...\\-&+&-&+&...\\&&...\end{bmatrix}$$
- **<u>Definition:</u>**
	- An upper-triangular matrix is a square matrix such that all entries below the diagonal are 0.
	- A lower-triangular matrix is a square matrix such that all entries above the diagonal are 0.
- **<u>Theorem:</u>**
	- If $A$ is either upper-triangular or lower-triangular, then $|A|$ is just the product of the diagonal entries.

### Properties of determinants
- I mean, it would be nice if we could just row reduce to an upper/lower-triangular matrix. But row operations don't preserve the determinant.
- We can, however, track what the effect is on the final product!
- **<u>Theorem:</u>**
	- Let $A$ be a square matrix.
		1. If a multiple of one row of $A$ is added to another row to produce a new matrix $B$, then $\text{det}(A)=\text{det}(B)$.
		2. If two rows of $A$ are switched to produce a new matrix $B$, then $\text{det}(A)=-\text{det}(B)$.
		3. If a row of $A$ is multiplied by a constant $c$ to produce a new matrix $B$, then $\text{det}(A)=\frac{1}{c}\text{det}(B)$.
	- Well this isn't bad at all!
- Example:
	- Compute the determinant of $A$, where $$A=\begin{bmatrix}2&-8&4\\-2&8&-9\\-1&7&2\end{bmatrix}$$
	- Let's set it up as: $$\text{det}(A)=\begin{vmatrix}2&-8&4\\-2&8&-9\\-1&7&2\end{vmatrix}$$
	- Alright, well let's multiply row 1 by $\frac{1}{2}$: $$\text{det}(A)=2\begin{vmatrix}1&-4&2\\-2&8&-9\\-1&7&2\end{vmatrix}$$
	- Next, let's add row 1 to row 2 twice: $$\text{det}(A)=2\begin{vmatrix}1&-4&2\\0&0&-5\\-1&7&2\end{vmatrix}$$
	- Now we can just add row 1 to row 3: $$\text{det}(A)=2\begin{vmatrix}1&-4&2\\0&0&-5\\0&3&2\end{vmatrix}$$
	- Nice! Now we can just swap rows to get a triangular matrix! $$\text{det}(A)=-2\begin{vmatrix}1&-4&2\\0&3&2\\0&0&-5\end{vmatrix}$$
	- From this, $\text{det}(A)=-2(1\cdot3\cdot-5)=-2(-15)=30$.
	- So $\text{det}(A)=30$.
- Due to some insane transitive property train of logic, we can prove this **<u>theorem:</u>**
	- $A$ is invertible $\iff$ $\text{det}(A)\ne 0$.