### Vector subspaces continued
- A subspace, $H$ of a vector space $V$ is itself a vector space.
- **<u>Examples:</u>**
	1. If $V$ is any vector space then:
		- $V$ is a subspace of itself.
		- $\{\overrightarrow{0}\}$ is a subspace called the <u>zero subspace</u>.
	2. $H=\left\{\begin{bmatrix}s\\2s\end{bmatrix}\ |\ s\in\mathbb{R}\right\}$ is a subspace of $\mathbb{R}^2$.
	3. $H=\left\{\begin{bmatrix}s\\t\\0\end{bmatrix}\ |\ s,t\in\mathbb{R}\right\}$ is the $x\text{-}y$ plane in $\mathbb{R}^3$, and a subspace of $\mathbb{R}^3$.
	4. Lines and planes ***NOT*** through the origin are ***<u>NOT SUBSPACES</u>***.
	5. $\mathbb{P}_n=\left\{\text{Polynomials of degree at most }n\right\}$ is a subspace of $\mathbb{P}=\left\{\text{Polynomials of any degree}\right\}$.
	6. $H=\left\{\begin{bmatrix}-a+b\\2a+3b\\b\end{bmatrix}\ |\ a,b\in\mathbb{R}\right\}$ is a subspace of $\mathbb{R}^3$ because $\begin{bmatrix}-a+b\\2a+3b\\b\end{bmatrix}$ is a span in $\mathbb{R}^3$.
- **<u>Theorem:</u>**
	- Let $V$ be a vector space. Let $\overrightarrow{v}_1,\overrightarrow{v}_2,...\overrightarrow{v})k\in V$.
	- $\text{Span}\left\{\overrightarrow{v}_1,...,\overrightarrow{v}_k\right\}$ is a subset of $V$ called the <u>subspace spanned by $\overrightarrow{v}_1,...,\overrightarrow{v}_k$</u>.
- **<u>Definition:</u>**
	- Let $A$ be an $m\text{x}n$ matrix. The <u>nullspace</u> of $A$ is the set of all vectors $\overrightarrow{v}\ |\ A\overrightarrow{v}=\overrightarrow{0}$.
	- In other words, $\text{Nul }A$ is the solution set of the equation $A\overrightarrow{x}=\overrightarrow{0}$.
	- $\text{Nul }A=\left\{\overrightarrow{v}\in\mathbb{R}^n\ |\ A\overrightarrow{v}=\overrightarrow{0}\right\}$
- **<u>Theorem:</u>**
	- $\text{Nul }A$ is a subspace of $\mathbb{R}^n$.
- **<u>Example:</u>**
	- Is the vector $\begin{bmatrix}1\\2\end{bmatrix}\in\text{Nul }\begin{bmatrix}-2 & 1\\2 & -1\\-4 & 2\end{bmatrix}$
	- Well, let's multiply the vector by the matrix and see if it's the zero vector, right? 
	- If we call this vector $\overrightarrow{x}$ and the above matrix $A$, then we have $A\overrightarrow{x}=\overrightarrow{0}$. That's the only thing that makes a vector go into the nullspace.
- **<u>Example:</u>**
	- $H=\left\{\begin{bmatrix}a\\b\\c\end{bmatrix}\in\mathbb{R}^3\ |\ 2a-b+3c=0\right\}$, is there a matrix $A$ that $H$ is the nullspace of?
	- Silly question, yes. It's the coefficient matrix of $2a-b+3c$!
	- $\begin{bmatrix}2 & -1 & 3\end{bmatrix}$.
- **<u>Comment:</u>**
	- Given $A$, if you want to express $\text{Nul }A$ as the span of a collection of vectors, row-reduce $A$ to find the general solution of $A\overrightarrow{x}=\overrightarrow{0}$, and then just write the solution in vector form within a span!
- **<u>Definition:</u>**
	- Let $A$ be an $m\text{x}n$ matrix. The <u>column space</u> of $A$, denoted $\text{Col }A$, is the span of the columns of $A$.
	- $A=\left[\overrightarrow{a}_1\ \ \overrightarrow{a}_2\ \ ...\ \ \overrightarrow{a}_n\right]$, $\text{Col }A=\text{Span}\left\{\overrightarrow{a}_1,...,\overrightarrow{a}_n\right\}$
	- It is a subspace of $\mathbb{R}^m$.
	- The <u>row space</u> of $A$ , denoted $\text{Row }A$, is the span of the rows of $A$. It is a subspace of $\mathbb{R}^n$.
	- $\text{Row }A=\text{Col }A^T$
- **<u>Example:</u>**
	- $A=\begin{bmatrix}1 & 0 & 1\\2& -1& 0\end{bmatrix}$. Determine $\text{Nul }A$, $\text{Col} A$, and $\text{Row }A$.
	- $\text{Col }A=\text{Span}\left\{\begin{bmatrix}1\\2\end{bmatrix},\begin{bmatrix}0\\-1\end{bmatrix},\begin{bmatrix}1\\0\end{bmatrix}\right\}$.
		- Notice that $\begin{bmatrix}x\\y\end{bmatrix}=x\begin{bmatrix}1\\0\end{bmatrix}+(-y)\begin{bmatrix}0\\-1\end{bmatrix}$, which shows that $\text{Col }A=\mathbb{R}^2$.
		- In general, we will need to some calculation to determine if a vector $\overrightarrow{b}$ belongs to $\text{Col }A$. It would need to be a check for if $A\overrightarrow{x}=\overrightarrow{b}$ is consistent.
		- We have concluded here that $A\overrightarrow{x}=\overrightarrow{b}$ is consistent $\forall\overrightarrow{b}\in\mathbb{R}^2$.
	- $\text{Row }A=\text{Span}\left\{\begin{bmatrix}1\\0\\1\end{bmatrix},\begin{bmatrix}2\\-1\\0\end{bmatrix}\right\}$ (subspace of $\mathbb{R}^3$, a plane).
	- $\text{Nul }A=\left\{\overrightarrow{x}\in\mathbb{R}^3\ |\ A\overrightarrow{x}=\overrightarrow{0}\right\}$.
		- To solve further, solve that equation in the augmented matrix: $$\begin{bmatrix}1 & 0 & 1 & 0\\2&-1&0&0\end{bmatrix}$$
		- This simplifies to: $$\begin{bmatrix}1 & 0 & 1 & 0\\0&1&2&0\end{bmatrix}$$
		- From this, we know: $$\overrightarrow{x}=\begin{bmatrix}x_1\\x_2\\x_3\end{bmatrix}=\begin{bmatrix}-x_3\\-2x_3\\x_3\end{bmatrix}=x_3\begin{bmatrix}-1\\-2\\1\end{bmatrix}$$
		- Which tells us that $\text{Nul }A=\text{Span}\left\{\begin{bmatrix}-1\\-2\\1\end{bmatrix}\right\}$.
- Comparison of $\text{Nul }A$ and $\text{Col }A$:

|$\text{Nul }A$|$\text{Col }A$|
|----------------|----------------|
|Subspace of $\mathbb{R}^n$|Subspace of $\mathbb{R}^m$|
|Defined by equations ($A\overrightarrow{x}=\overrightarrow{0}$)|Defined as $\text{Span}\left\{\overrightarrow{a}_1,...,\overrightarrow{a}_n\right\}$|
|Finding vectors in the nullspace takes work|Finding vectors is easy, just take any linear combination.|
|$\overrightarrow{v}\in\text{Nul }A$ satisfies $A\overrightarrow{v}=\overrightarrow{0}$|$\overrightarrow{v}\in\text{Col }A$ satisfies $A\overrightarrow{x}=\overrightarrow{v}$ is consistent|
|It's easy to test if $\overrightarrow{v}\in\text{Nul }A$, just multiply $A$ and $\overrightarrow{v}$.|Takes work to check if $\overrightarrow{v}\in\text{Col }A$, check if the system is consistent (Row reduce $\left[A\ \ \overrightarrow{v}\right]$.|
|$\text{Nul }A=\left\{\overrightarrow{0}\right\}$ happens iff $A\overrightarrow{x}=\overrightarrow{0}$ has only the trivial solution (columns of $A$ are LI, $\text{T}\left(\overrightarrow{x}\right)=A\overrightarrow{x}$ is one-one).|$\text{Col }A=\mathbb{R}^m$ happens iff $A\overrightarrow{x}=\overrightarrow{b}$ is consistent for any $\overrightarrow{b}$ ($\text{T}\left(\overrightarrow{x}\right)=A\overrightarrow{x}$ is onto). |

- Just like we generalize $\mathbb{R}^n$ as a vector space, we can also generalize the idea of a linear transformation.
- **<u>Definition:</u>**
	- Let $V, W$ be vector spaces.
	- A linear transformation $\text{T}$ from $V$ to $W$ is a rule that assigns to each vector, $\overrightarrow{v}\in V$ a vector $\text{T}\left(\overrightarrow{v}\right)\in W$.
	- It must satisfy:
		- $\text{T}\left(\overrightarrow{u}+\overrightarrow{v}\right)=\text{T}\left(\overrightarrow{u}\right)+\text{T}\left(\overrightarrow{v}\right)$
		- $\text{T}\left(c\overrightarrow{u}\right)=c\text{T}\left(\overrightarrow{u}\right)$
- **<u>Example:</u>**
	- Let's take $\mathbb{P}$.
	- Our transformation will be $\text{T}=\frac{d}{dt}$. This goes from $V=\mathbb{P}$ to $W=\mathbb{P}$.
	- I mean, derive a polynomial and you get another polynomial of degree $n-1$, so we're good here. Derive with respect to $t$ and we have a transformation!
	- Derivatives can have constants factored out and split on addition, so everything is satisfied for a valid transformation.
	- In some sense, $\text{Calculus}\subset\text{Linear Algebra}$!
- **<u>Definition:</u>**
	- Let $\text{T}:V\longrightarrow W$ be a linear transformation. Then the <u>kernel</u> of $\text{T}$ is the set of all vectors $\overrightarrow{v}\in V\ |\ \text{T}\left(\overrightarrow{v}\right)=\overrightarrow{0}$.
	- The <u>range</u> of $\text{T}$ is the set of all vectors $\overrightarrow{w}\in W\ |\ \overrightarrow{v}\in V\ |\ \text{T}\left(\overrightarrow{v}\right)=\overrightarrow{w}$.
	- $\text{Nul }A=\text{Kernel T}$, $\text{Col }A=\text{Range T}$.
- **<u>Example:</u>**
	- $V=W=\mathbb{P}$
	- $\text{T}=\frac{d}{dt}$
	- $\text{Kernel T}=\mathbb{R}$ (derivative of a constant is 0)
	- $\text{Range T}=\mathbb{P}$ (by integration/common sense)