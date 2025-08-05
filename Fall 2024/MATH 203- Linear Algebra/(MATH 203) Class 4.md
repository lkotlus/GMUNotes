We up in here doing math and whatnot.

## Continuing to explore

### New Notation
- We want something for the set of all n-dimensional vectors.
- Here's the notation: $\mathbb{R}^n$ denotes the set of all n-dimensional vectors.
	- $\mathbb{R}^2$ - $xy$ plane
	- $\mathbb{R}^3$ - typical three dimensional space
	- $\mathbb{R}^4$ - set of all vectors that fit $\begin{bmatrix}a_1\\a_2\\a_3\\a_4\end{bmatrix}$
	- ...

### The matrix equation: $A\overrightarrow{x}=\overrightarrow{b}$
- Let $A$ be an $m$x$n$ matrix.
- Let $\overrightarrow{a}_1, \overrightarrow{a}_2, ..., \overrightarrow{a}_n$ be the columns of A.
- Let $\overrightarrow{x}=\begin{bmatrix}x_1\\x_2\\...\\x_n\end{bmatrix}$
- Insert definitions to get $A\overrightarrow{x}=\begin{bmatrix}a_1 & a_2 & ... & a_n\end{bmatrix}\begin{bmatrix}x_1\\x_2\\...\\x_n\end{bmatrix}$
- Note that there must be an equal number of columns in $A$ as the number of rows in $\overrightarrow{x}$.
- From this, $A\overrightarrow{x}=x_1\overrightarrow{a}_1+x_2\overrightarrow{a}_2+...+x_n\overrightarrow{a}_n$.
- Example:
	- $A=\begin{bmatrix}1&2&3\\4&5&6\end{bmatrix}$, $\overrightarrow{x}=\begin{bmatrix}-1\\1\\2\end{bmatrix}$
	- From this, we know that $A\overrightarrow{x}=(-1)\begin{bmatrix}1\\4\end{bmatrix} + 1\begin{bmatrix}2\\5\end{bmatrix} + 2\begin{bmatrix}3\\6\end{bmatrix}$
	- Simplifying, $A\overrightarrow{x}=\begin{bmatrix}-1\\-4\end{bmatrix} + \begin{bmatrix}2\\5\end{bmatrix} + \begin{bmatrix}6\\12\end{bmatrix}$
	- Further, $A\overrightarrow{x}=\begin{bmatrix}7\\13\end{bmatrix}$
- Something worth noting: $A\overrightarrow{x}=\begin{bmatrix}A_1\cdot x_1\\A_2\cdot x_2\\...\\A_n\cdot x_n\end{bmatrix}$ (Dot product each row of $A$ with each column of $x$)

### Properties of $A\overrightarrow{x}=\overrightarrow{b}$
- $A(\overrightarrow{x}+\overrightarrow{y})=A\overrightarrow{x}+A\overrightarrow{y}$
- $A(c\overrightarrow{x})=c(A\overrightarrow{x})$

### Practical application
- Suppose we have a system of equations (I'm sensing a them to this class)
$$
-x_1+3x_2-x_3=-7
$$
$$
2x_1+x_2=1
$$
- We know how to write this as a single vector equation:
$$
x_1\begin{bmatrix}-1\\2\end{bmatrix} + x_2\begin{bmatrix}3\\1\end{bmatrix} + x_3\begin{bmatrix}-1\\0\end{bmatrix} = \begin{bmatrix}-7\\1\end{bmatrix}
$$
- We now see we can write this as:
$$
\begin{bmatrix}-1&3&-1\\2&1&0\end{bmatrix}\begin{bmatrix}x_1\\x_2\\x_3\end{bmatrix}=\begin{bmatrix}-7\\1\end{bmatrix}
$$
- In the above we can see that this is just $A\overrightarrow{x}=\overrightarrow{b}$!
- **Summary**
	- $A=[\overrightarrow{a}_1\,\,\, \overrightarrow{a}_2\,\,\, ...\,\,\, \overrightarrow{a}_3]$, $\overrightarrow{b}$ in $\mathbb{R}^m$, then $A\overrightarrow{x}=\overrightarrow{b}$ has the same set of solutions as the vector equation $A\overrightarrow{x}=x_1\overrightarrow{a}_1+x_2\overrightarrow{a}_2+...+x_n\overrightarrow{a}_n$, which in turn has the same set of solutions as the system of equations with augmented matrix $[\overrightarrow{a}_1\,\,\, \overrightarrow{a}_2\,\,\, ...\,\,\, \overrightarrow{a}_3\,\,\,\overrightarrow{b}]$

### Another example
- Let $A=\begin{bmatrix}1&0&1\\1&1&0\\-1&-2&1\end{bmatrix}$.
- Is the system $A\overrightarrow{x}=\overrightarrow{b}$ consistent for all $\overrightarrow{b}$?
- Being consistent means that $\overrightarrow{b}$ is a linear combination of the columns of $A$.
- That just means that $\overrightarrow{b}$ is in $Span\{\overrightarrow{a}_1, \overrightarrow{a}_2, \overrightarrow{a}_3\}$!
- So the question is really just asking if $\mathbb{R}^3=Span\{\overrightarrow{a}_1, \overrightarrow{a}_2, \overrightarrow{a}_3\}$!
- Well we have three vectors in $\mathbb{R}^3$, so as long as none of these vectors are parallel we should be good.
- Let's work this out...
$$
\begin{bmatrix}
1&0&1&b_1\\
1&1&0&b_1\\
-1&-2&1&b_3
\end{bmatrix}
$$
$$
\begin{bmatrix}
1&0&1&b_1\\
0&1&-1&b_2-b_1\\
0&-2&2&b_3+b_1
\end{bmatrix}
$$
$$
\begin{bmatrix}
1&0&1&b_1\\
0&1&-1&b_2-b_1\\
0&0&0&b_3+2b_2-b_1
\end{bmatrix}
$$
- We can see that this won't always be consistent! We would need $b_3+2b_2-b_1$ to always be 0, but that won't always be the case!
- From this, we know that not all values of $\overrightarrow{b}$ are consistent and that $\mathbb{R}^3\ne Span\{\overrightarrow{a}_1, \overrightarrow{a}_2, \overrightarrow{a}_3\}$.
- It is worth noting that $b_3+2b_2-b_1=0$ is a plane in $\mathbb{R}^3$.
- The system will be consistent for all values of $\overrightarrow{b}$ if we didn't have any zero rows.
- **Theorem**:
	- Let $A$ be a matrix. Then the following are equivalent:
		1. For every $\overrightarrow{b}$ in $\mathbb{R}^m$, $A\overrightarrow{x}=\overrightarrow{b}$ is consistent.
		2. Every $\overrightarrow{b}$ in $\mathbb{R}^m$ is a linear combination of the columns of $A$.
		3. The columns of $A$ span $\mathbb{R}^m$.
		4. $\text{RREF}(A)$ has a pivot in every row

### In-class work
1. The system of equations can be written as:
$$\begin{matrix}
x_1+x_2=1\\
-x_1=0\\
x_1+x_2=2
\end{matrix}
$$
Or as an augmented matrix,
$$
\begin{bmatrix}
1&1&1\\
-1&0&0\\
1&1&2
\end{bmatrix}
$$
2. True.
3. Getting to RREF:
$$
\begin{bmatrix}
1&1&1\\
-1&0&0\\
1&1&2
\end{bmatrix}
$$
$$
\begin{bmatrix}
1&1&1\\
0&1&1\\
1&1&2
\end{bmatrix}
$$
$$
\begin{bmatrix}
1&1&1\\
0&1&1\\
0&0&1
\end{bmatrix}
$$
$$
\begin{bmatrix}
1&0&0\\
0&1&1\\
0&0&1
\end{bmatrix}
$$
4. The system is not consistent ($0\ne 1$).