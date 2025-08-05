
## Linear independence
- Homogeneous systems
	- They look like $A\overrightarrow{x}=\overrightarrow{0}$.
	- They're always consistent, because you always have the trivial solution: $\overrightarrow{x}=\begin{bmatrix}0\\0\\...\\0\end{bmatrix}$.
- If we think about a homogeneous system in vector form, we get:
$$
x_1\overrightarrow{a}_1 + x_2\overrightarrow{a}_2 + ... + x_k\overrightarrow{a}_k = \overrightarrow{0}
$$
$$
A = \begin{bmatrix}\overrightarrow{a}_1 & \overrightarrow{a}_2 & ... \overrightarrow{a}_k\end{bmatrix}
$$
$$
\overrightarrow{x} = \begin{bmatrix}x_1\\x_2\\...\\x_k\end{bmatrix}
$$
- **Definition!**
	- A set of vectors $\{\overrightarrow{a}_1,\, \overrightarrow{a}_2,\, ...,\, \overrightarrow{a}_k\}$ is **linearly independent (LI)** if the only solution of $x_1\overrightarrow{a}_1 + x_2\overrightarrow{a}_2 + ... + x_k\overrightarrow{a}_k = \overrightarrow{0}$ is the trivial solution $x_1=x_2=...=x_k=0$.
	- The set $\{\overrightarrow{a}_1,\, \overrightarrow{a}_2,\, ...,\, \overrightarrow{a}_k\}$ is **linearly dependent (LD)** if there are numbers $c_1,\, c_2,\, ...,\, c_k$ that are not all zero such that $c_1\overrightarrow{a}_1 + c_2\overrightarrow{a}_2 + ... + c_k\overrightarrow{a}_k = \overrightarrow{0}$. 
	- It makes sense to call it independent if they're always zero, because the components of $\overrightarrow{x}$ are independent of one another if they are always 0. They are dependent in the other scenario because they have some sort of relationship between one another that makes it so.
- Example!
	- Look at the vectors: $$\overrightarrow{a}_1=\begin{bmatrix}1\\0\\1\end{bmatrix},\,\overrightarrow{a}_2=\begin{bmatrix}-1\\2\\1\end{bmatrix},\,\overrightarrow{a}_3=\begin{bmatrix}1\\2\\3\end{bmatrix}$$
	- Determine whether $\{\overrightarrow{a}_1,\,\overrightarrow{a}_2,\,\overrightarrow{a}_3\}$ is LI or LD. If it is LD, provide a linear dependence relation.
	- This is easy. Just find a nontrivial solution by finding all solutions.
	- Well, let's just put our augmented matrix: $$\begin{bmatrix}1 & -1 & 1 & 0\\0 & 2 & 2 & 0 \\1 & 1 & 3 & 0 \ \end{bmatrix}$$
	- Solving, we find that our solution is: $$\overrightarrow{x}=\begin{bmatrix}x_1\\x_2\\x_3\end{bmatrix} = \begin{bmatrix}-2x_3\\-x_3\\x_3\end{bmatrix} = x_3\begin{bmatrix}-2\\-1\\1\end{bmatrix}$$
	- This gives us the answer to our original question: we have a nontrivial solution, therefore the set of vectors is LD.
- Some comments about this:
	- If we are LD, then we have all three vectors trapped in the same plane. (Geometric stuff)
	- We can also see that we can write a vector equation like: $\overrightarrow{a}_3=2\overrightarrow{a}_1 + \overrightarrow{a}_2$. That means that $\overrightarrow{a}_3$ is just the result of a vector addition between the two others. That makes the plane make more sense. 
	- Essentially, $\text{Span}\{\overrightarrow{a}_1,\,\overrightarrow{a}_2,\,\overrightarrow{a}_3\}$ is a plane.
- What are the results of being LD?
	- We can now say $A\overrightarrow{x}=\overrightarrow{0}$ has only the trivial solution iff the columns of $A$ are LI.
- A set $\{\ \overrightarrow{a}\ \}$ is LD if $\overrightarrow{a} \ne \overrightarrow{0}$ and is LD if $\overrightarrow{a}=\overrightarrow{0}$.
- A set $\{\overrightarrow{a}_1,\ \overrightarrow{a}_2\}$ is LD if and only if $\overrightarrow{a}_1$ is a scalar multiple of $\overrightarrow{a}_2$ (or vice-reversa).
- **Theorem:**
	- If you have a set of vectors, $S=\{\overrightarrow{a}_1, \ ..., \ \overrightarrow{a}_k\}$ is LD if and only if at least one vector in $S$ is a linear combination of the others. 
	- This also means that we can easily check it by seeing if some vector in $S$ is in the span of all other vectors in $S$.
- Example:
	- Are the following vectors LI or LD? $$\overrightarrow{u}=\begin{bmatrix}1\\1\\0\end{bmatrix}, \ \overrightarrow{v}=\begin{bmatrix}2\\3\\0\end{bmatrix}$$
	- We know, by inspection, that neither are a scalar multiple of each other. From this, we are LI.
- Further example from that.
	- Take the above vectors, and add an unknown vector $\overrightarrow{w}$. What would make it LD or LI?
	- Well, we know that we are LD if $\overrightarrow{w} \in \text{Span}\{\overrightarrow{u}, \ \overrightarrow{v}\}$!
	- Our vectors are pretty simple, and we can see based on their components that they are exclusively in $\mathbb{R}^2$, so that means the span is $\mathbb{R}^2$. From this, if $\overrightarrow{w}\in\mathbb{R}^2$, we have are LD. Otherwise, we are LI.
- Another example:
	- Suppose $\overrightarrow{a}_1, \ ..., \ \overrightarrow{a}_k$ are vectors in $\mathbb{R}^n$ and suppose $k>n$. 
	- To determine whether $S$ is LD or LI, we look at the system $$x_1\overrightarrow{a}_1+...+x_k\overrightarrow{a}_k=\overrightarrow{0}$$ $$\begin{bmatrix}\overrightarrow{a}_1 & ... & \overrightarrow{a}_k & \overrightarrow{0}\end{bmatrix}$$
	- Free variables mean LD, so if we have more columns than rows, we must have at least one free variable! We do have more columns than rows!!!
- Theorem from the above:
	- If $S=\{\overrightarrow{a}_1, \ ..., \ \overrightarrow{a}_k\}$ is a set of vectors in $\mathbb{R}^n$ and $k>n$, then $S$ is LD.

## In-class homework!
1. The free variables are $x_3$ and $x_4$.
	- We know this because we can see they are the only ones without leading entries.
2. Aight...
	- Start with our augmented matrix... $$\begin{bmatrix}1 & 0 & -2 & 1 & 0\\0 & 1 & 3 & -1 & 0\\0 & 0 & 0 & 0 & 0\ \end{bmatrix}$$
	- We're already in RREF, so now we can just do some algebra: $$x_1=2x_3-x_4$$ $$x_2=x_4-3x_3$$
3. So from this, we can say that $$\overrightarrow{x}=\begin{bmatrix}x_1\\x_2\\x_3\\x_4\end{bmatrix}=\begin{bmatrix}2x_3-x_4\\x_4-3x_3\\x_3\\x_4\end{bmatrix}=x_3\begin{bmatrix}2\\-3\\1\\0\end{bmatrix}+x_4\begin{bmatrix}-1\\1\\0\\1\end{bmatrix}$$
4.  $S = \text{Span}\{\overrightarrow{u}, \ \overrightarrow{v}\ \}$ with the following definitions for $\overrightarrow{u}$ and $\overrightarrow{v}$: $$\overrightarrow{u} = x_3\begin{bmatrix}2\\-3\\1\\0\end{bmatrix}, \ \overrightarrow{v}=x_4\begin{bmatrix}-1\\1\\0\\1\end{bmatrix}$$