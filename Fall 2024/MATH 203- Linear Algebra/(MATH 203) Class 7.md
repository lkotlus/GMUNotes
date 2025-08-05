# EXAM NEXT WEEK
- "Practice problems lie on the more difficult side."
- "The midterm will be less difficult than the practice problems."

## Linear transformations
### Transformations
- Robots in disguise.
- A **transformation** (or function or map) $\text{T}$ from $\mathbb{R}^n$ to $\mathbb{R}^m$ is a rule that assigns to each vector $\overrightarrow{x}$ in $\mathbb{R}^n$ a vector $\text{T}(\overrightarrow{x})$ in $\mathbb{R}^m$.
	- $\mathbb{R}^n$ - the domain of $\text{T}$
	- $\mathbb{R}^m$ - the codomain of $\text{T}$
- And we use the notation: $$\text{T}:\, \mathbb{R}^n \rightarrow \mathbb{R}^m$$
- To summarize this:
	- $\overrightarrow{x}\in \mathbb{R}^n$ - "$\overrightarrow{x}$ belongs to $\mathbb{R}^n$"
	- $\text{T}(\overrightarrow{x}) \in \mathbb{R}^m$ is called the image of $\overrightarrow{x}$ (under $\text{T}$).
	- The set of all images $\{\text{T}(\overrightarrow{x})\ \ | \ \ \overrightarrow{x} \in \mathbb{R}^n \}$ is called the range of $\text{T}$.

### Matrix transformations
- Let $\text{A}$ be an $m\text{x}n$ matrix. If $\overrightarrow{x} \in \mathbb{R}^n$, then $\text{A}\overrightarrow{x}\in\mathbb{R}^m$.
- So we have a normal transformation:
	- $\text{T}:\ \mathbb{R}^n \rightarrow \mathbb{R}^m$
- Now we have a *matrix* transformation:
	- $\text{T}(\overrightarrow{x}) = \text{A}\overrightarrow{x}$
- $\text{range}(\text{T}) = \{\text{A}\overrightarrow{x}\ \ | \ \ \overrightarrow{x}\in\mathbb{R}^n\} = \text{Span}\{\overrightarrow{a}_1, \overrightarrow{a}_2, ..., \overrightarrow{a}_3\}$
- The range of $\text{T}$ is the span of the columns of $\text{A}$.
- Example time:
	- Yo, check this scenario... $$\text{A}=\begin{bmatrix}1 & 2\\3 & -3 \\ -2 & -1\end{bmatrix}, \ \ \text{T}(\overrightarrow{x}) = \text{A}\overrightarrow{x}$$
	- This tells us that $\text{T}: \mathbb{R}^2 \rightarrow \mathbb{R}^3$.
	- Given $\overrightarrow{b}\in\mathbb{R}^3$, how would we determine if $\overrightarrow{b}$ is in $\text{range}(\text{T})$?
	- Rephrase with math: does $\text{T}(\overrightarrow{x})=\overrightarrow{b}$?
	- Rephrase with math again: does $\text{A}\overrightarrow{x}=\overrightarrow{b}$?
	- Well we know it is really just asking if $\overrightarrow{b}$ is in the span of the columns of $\text{A}$, so just set $\overrightarrow{b}$ to the solution of our matrix equation $\text{A}\overrightarrow{x}=\overrightarrow{b}$. If we row reduce into solutions then we have $\overrightarrow{b}$ in the span. 
	- What if we were to ask if there is a vector $\overrightarrow{x}$ such that $\text{T}(\overrightarrow{x})=\overrightarrow{b}$ is unique?
	- If we have free variables then the solution is not unique. If there is one unique solution, we're good to go.
	- If $\overrightarrow{b}=\overrightarrow{0}$, then the solution is unique iff the columns of $\text{A}$ are linearly independent.

### More examples of matrix transformations
- This one is fun:
	- Take the following scenario: $$\text{A}=\begin{bmatrix}1 & 0 & 0\\0 & 1 & 0\\0 & 0 & 1\end{bmatrix}, \ \ \text{T}(\overrightarrow{x})=\text{A}\overrightarrow{x}, \ \ \text{T}=\mathbb{R}^3\rightarrow\mathbb{R}^3$$
	- Think about it for a sec... $$\text{T}(\overrightarrow{x})=\text{A}\overrightarrow{x}=x_1\overrightarrow{a}_1+...=\overrightarrow{x}$$
	- We just get the original vector out again! This means we have the identity matrix for $\mathbb{R}^3$. Identity matrix is always just diagonal ones with zeroes surrounding.
- Math genius...
	- So for this, $$\text{A}=\begin{bmatrix}0 & 0 & 0\\0 & 1 & 0\\0 & 0 & 1\end{bmatrix}$$
	- If you think about this, this will just remove the $x_1$ component of our resulting matrix.
	- That means we just get the projection of the input matrix on the $x_2$$x_3$-plane!
- You cannot row reduce $\text{A}$ in a linear transformation!!!
- This is interesting...
	- So with this matrix: $$\text{A}=\begin{bmatrix}r & 0\\0 & r \end{bmatrix}$$
	- So $r$ is some number. This just scales the input vector by $r$, and is called a **dilation by a factor of r**.
	- If $r=1$, then we just have the identity matrix, which is a dilation by a factor of 1.

### Big definition
- A transformation $\text{T}: \mathbb{R}^n\rightarrow\mathbb{R}^m$ is linear if
	1. $\text{T}(\overrightarrow{u}+\overrightarrow{v}) = \text{T}(\overrightarrow{u})+\text{T}(\overrightarrow{v})$
	2. $\text{T}(c\overrightarrow{u})=c\text{T}(\overrightarrow{u})$
- For all $\overrightarrow{u},\overrightarrow{v}\in\mathbb{R}^n$ and all $c\in\mathbb{R}$ matrix transformations are linear due to the properties of matrix multiplication!
- Note that if we set $c=0$, then $\text{T}(\overrightarrow{0})=\overrightarrow{0}$
- Example:
	- $\text{T}\begin{bmatrix}x_1\\x_2\\x_3\end{bmatrix}=\begin{bmatrix}x_1\\x_2\\x_3+1\end{bmatrix}$
	- This is NOT linear, because $\text{T}(\overrightarrow{0})\ne\overrightarrow{0}$
- The first and second qualifications for linear combinations can be combined such that: $\text{T}(c\overrightarrow{u}+d\overrightarrow{v}) = c\text{T}(\overrightarrow{u})+d\text{T}(\overrightarrow{v})$. 
	- This means that $\text{T}$ preserves linear combinations (you get a linear combination in and a linear combination out).

### Cool example:
- Take the following transformation:$$\text{A}=\begin{bmatrix}0 & -1\\1 & 0 \end{bmatrix}$$
- This creates a vector orthogonal to the input one!