### Midterm 1 info
- Mean: 16.2/24
- Median: 16.5/24
- I have reached heights of genius on the levels of the vinci, new ton, and ray man.

### Characterizations of invertible matrices
- Let's say you have a system of equations (*in this class, really?!*), $A\overrightarrow{x}=\overrightarrow{b}$. A solution exists  $\forall\overrightarrow{b}\iff$ every row of $\text{RREF}(A)$ has a pivot. (The columns of the $n\text{x}m$ matrix $A$ span $\mathbb{R}^m$)
- Solution is unique $\forall$ valid $\overrightarrow{b}\iff$ every column of $\text{RREF}(A)$ has a pivot.
- That means that a for a square matrix:
	- Unique solution exists $\forall\overrightarrow{b}\iff$ either every column or every row of $\text{RREF}(A)$ has a pivot.
	- In other words, if $A$ is square, there is a pivot in each row of $\text{RREF}(A)\iff$ there is a pivot in each column of $\text{RREF}(A)$.
	- Pigeonhole!
- **<u>Recall the definition of invertible:</u>**
	- $A$ is invertible if $\exists$ a matrix $B$ $|$ $AB=I_n=BA$. 
- **<u>Invertible matrix theorem:</u>**
	- Let $A$ be a square $n\text{x}n$ matrix, then the following statements are equivalent:
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
	- **Comment**: 9 and 10 say that it is enough to have just one of these equations on a square matrix to say that it is invertible.
- **<u>What about for linear transformations?</u>**
	- **Definition**:
		- A linear transformation $\text{T}: \mathbb{R}^n\rightarrow\mathbb{R}^n$ is invertible if there is a linear transformation $\text{S}: \mathbb{R}^n\rightarrow\mathbb{R}^n$ that undoes $\text{T}$.
		- In other words, if $\text{T}$ has an inverse transformation such that $\text{T}\left(\text{S}\left(\overrightarrow{x}\right)\right)=\overrightarrow{x} \land \text{S}\left(\text{T}\left(\overrightarrow{x}\right)\right)=\overrightarrow{x} \ \ \ \forall \overrightarrow{x}$
- **<u>Theorem:</u>**
	- Let $\text{T}: \mathbb{R}^n\rightarrow\mathbb{R}^n$ be a linear transformation, $\text{T}\left(\overrightarrow{x}\right)=A\overrightarrow{x}$.
	- $\text{T}$ is invertible $\iff A$ is invertible.
	- In this case, $\text{T}^{-1}\left(\overrightarrow{x}\right)=A^{-1}\overrightarrow{x}$.

### In-class true/false questions (assume $A$ is $n\text{x}n$)
1. If the columns of $A$ span $\mathbb{R}^n$, then the columns of $A$ are LI.
	- True! By the theorem.
2. $A\overrightarrow{x}=\overrightarrow{b}$ has exactly one solution $\forall\overrightarrow{b}\in\mathbb{R}^n$.
	- False! We have no reason to come to this conclusion.
3. If $A\overrightarrow{x}=\overrightarrow{b}$ has at most one solution $\forall\overrightarrow{b}$, then it has exactly one solution $\forall\overrightarrow{b}$
	- True! By the theorem.
4. If $A\overrightarrow{x}=\overrightarrow{0}$ has a non-trivial solution, then $A$ cannot be row-reduced to $I_n$.
	- True! By the theorem (negation of the statements).
5. If there is a vector $\overrightarrow{b} \ \ | \ \ A\overrightarrow{x}=\overrightarrow{b}$ is inconsistent, then $\text{T}\left(\overrightarrow{x}\right)=A\overrightarrow{x}$ is not one-one.
	- True! Also negation.
6. If two columns of $A$ are identical, then $A$ is not invertible.
	- True!
7. If $A\overrightarrow{x}=\overrightarrow{0}$ has a non-trivial solution.
	- False! Zero row!