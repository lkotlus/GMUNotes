We up here in math class for real.

### Pre-lecture
- The locations when going into REF that work as our first entries are called the pivot positions, the values within them are called the pivots, and the columns containing them are called the pivot columns.
- Columns that don't get leading entries will always be free variables.

### Vector equations
- Both direction and magnitude.
- Really, it's a single column matrix.
	- A matrix with a single column is called a vector
- The following is a matrix: 
$$
\begin{bmatrix}
1 \\
-2 \\
4
\end{bmatrix}
$$
- A vector with two entries is just a two dimensional vector. Epic. The general form we're working with is:
$$
\begin{bmatrix}
\,\,\, \overrightarrow{i} \,\,\, \\
\,\,\, \overrightarrow{j} \,\,\, \\
\,\,\, \overrightarrow{k} \,\,\, \\
\end{bmatrix}
$$
- Vector addition and whatnot is the same.
- We can scale vectors, just multiply into each row.
- $\overrightarrow{0}$ is the zero vector, it can be thought of as:
$$
\begin{bmatrix}
0 \\
0 \\
0 \\
... \\
0
\end{bmatrix}
$$
- Algebraic properties:
	- $\overrightarrow{u} + \overrightarrow{v} = \overrightarrow{v} + \overrightarrow{u}$
	- $(\overrightarrow{u} + \overrightarrow{v}) + \overrightarrow{w} = \overrightarrow{u} + (\overrightarrow{v} + \overrightarrow{w})$
	- $\overrightarrow{u} + \overrightarrow{0} = \overrightarrow{u}$
	- $\overrightarrow{u} + (-1)\overrightarrow{u} = \overrightarrow{0}$
	- ...

### Spans
- Let $\overrightarrow{a}_1, \overrightarrow{a}_2, \overrightarrow{a}_3, ..., \overrightarrow{a}_k$ be n-dimensional vectors.
- A vector of the form $c_1\overrightarrow{a}_1 + c_2\overrightarrow{a}_2 + c_3\overrightarrow{a}_3 + ... + c_k\overrightarrow{a}_k$ is called a **linear combination** of Let $\overrightarrow{a}_1, ..., \overrightarrow{a}_k$.
- The set of all linear combinations of $\overrightarrow{a}_1, ..., \overrightarrow{a}_k$ is called the **span** of $\overrightarrow{a}_1, ..., \overrightarrow{a}_k$, and the notation is $Span\{\overrightarrow{a}_1, ..., \overrightarrow{a}_k\}$
- This LaTeX is a nightmare.
- The span is literally just the line at the angle of the vector. That's the whole thing. Just expand it. Get it? ex(SPAN)d it! This is only the case for a *single* vector, though.
- Let's look at an example:
$$
\overrightarrow{a}_1 = \begin{bmatrix}1\\2\\0\end{bmatrix}
$$
$$
\overrightarrow{a}_2 = \begin{bmatrix}1\\2\\0\end{bmatrix}
$$
- So we know we are working with $c_1\overrightarrow{a}_1+c_2\overrightarrow{a}_2$. If you think about every possible value of $c_1$ and $c_2$, then it is clear that we are creating a plane that contains $\overrightarrow{a}_1$ and $\overrightarrow{a}_2$. Pretty cool.

### Is my vector in a span of other vectors?
- How do you determine if a vector, $\overrightarrow{b}$ is in the span of some other vectors $\overrightarrow{a}_1, ..., \overrightarrow{a}_k$?
- Well we just need to find $c_1, ..., c_k$ such that $c_1\overrightarrow{a}_1 + ... + c_k\overrightarrow{a}_k = \overrightarrow{b}$. 
- This is a vector equation!
- Let's define some stuff...
$$
\overrightarrow{a}_1 = \begin{bmatrix}a_{11}\\a_{12}\\...\\a_{1n}\end{bmatrix}
$$
$$
\overrightarrow{a}_k = \begin{bmatrix}a_{k1}\\a_{k2}\\...\\a_{kn}\end{bmatrix}
$$
- From this, we can sort of see that our full on equation is really:
$$
c_1\begin{bmatrix}a_{11}\\a_{12}\\...\\a_{1n}\end{bmatrix} + ... + c_k\begin{bmatrix}a_{k1}\\a_{k2}\\...\\a_{kn}\end{bmatrix}
=
\begin{bmatrix}b_1\\b_2\\...\\b_n\end{bmatrix}
$$
- Expand this, out and we'll see that we have:
$$
\begin{bmatrix}c_1a_{11} + ... + c_ka_{k1}\\
c_1a_{12} + ... + c_ka_{k2} \\
... \\
c_1a_{1n} + ... + c_ka_{kn}
\end{bmatrix}
=
\begin{bmatrix}b_1\\b_2\\...\\b_n\end{bmatrix}
$$
- This looks an awful lot like a system of equations! Let's replace $c$ with $x$ and go into an augmented matrix, and then you really get it.
$$
\begin{bmatrix}x_1a_{11} & ... & x_ka_{k1} & b_1\\
x_1a_{12} & ... & x_ka_{k2} & b_2 \\
... & ... & ... & ... \\
x_1a_{1n} & ... & x_ka_{kn} & b_n\end{bmatrix}
$$