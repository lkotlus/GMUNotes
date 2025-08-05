Math! *Math Algorithms...* **MATH ALGORITHMS!!!**

### Some more definitions
- **Leading Entry** is the first nonzero entry in a row
- A matrix is in **row echelon form** (REF) if
	1. All zero rows are at the bottom
	2. Each leading entry is to the right of the leading entry of the row above it
	3. All entries in a column below a leading entry are zero
- A matrix is in **reduced row echelon form** (RREF) if, in addition...
	1. Leading entry in each nonzero row is 1
	2. Each leading 1 is the only nonzero entry in its column

### Some examples
- Look at this matrix:
$$
\begin{bmatrix}
1 & 2 \\
0 & 3
\end{bmatrix}
$$
- That matrix is in REF, as it satisfies our conditions.
- Look at another one:
$$
\begin{bmatrix}
4 & 0 \\
0 & 0
\end{bmatrix}
$$
- This is in REF too, because there are no leading entries in the zero row and the zero row is at the bottom.
- Look at this one, it's going to be in RREF!
$$
\begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1 \\
\end{bmatrix}
$$
- We keep zero rows for everyone's favorite math concept... **convention**!
- These matrices don't need to be square either, so the following is still RREF:
$$
\begin{bmatrix}
1 & -2 & 0 \\
0 & 0 & 2 \\
\end{bmatrix}
$$
- So our goal is to find a way to use row elimination to get things into RREF

### Row reduction
- Given any matrix, there exists a sequence of elementary row operations, that brings the matrix to REF or RREF. This process is called **row reduction**.
- **FACT**:
	- The RREF of a matrix is unique, it does not depend on the elementary row operations used

### Row reduction **algorithm**
- Let's remind ourselves of the elementary row operations:
	1. Add a multiple of a row to another row
	2. Interchange two rows
	3. Multiply a row by a nonzero constant
- We shall use these in an algorithm to get any matrix to REF.
	- Find the first nonzero column
	- Use operation 2 to move your row to the top
	- Eliminate all other nonzero entries in that column with operation 1
	- Move to next column.
- This is so nice and elegant, I love it.
- If we want RREF:
	- Find the first nonzero column
	- Use 3 to make the leading nonzero entry 1
	- Use operation 2 to move your row to the top
	- Eliminate all other nonzero entries in that column with operation 1
	- Eliminate all nonzero entries above the current entry in the full matrix
	- Move to next column in a reduced matrix

### Solving a system
- Turn it into a matrix
- Find RREF with our algorithm
- If zero rows have a nonzero value, then the system is inconsistent
- If a variable has no column with a leading entry, it is called a **free variable**, and it must be solved for.
- Turn the RREF back into a system of equations and use them to solve for the remaining variables.
- Example:
	- Say the RREF of a system is:
$$
\begin{bmatrix}
1 & -3 & 0 & 4 & 0 & 0 \\
0 & 0 & 1 & -7 & 0 & -1 \\
0 & 0 & 0 & 0 & 1 & 4
\end{bmatrix}
$$
- This system is consistent, that's good. Let's go back to a system of equations.
$$
\begin{array}{l}
x_1 - 3x_2 + 4x_4 = 0 \\
x_3 - 7x_4 = -1 \\
x_5 = 4
\end{array}
$$
- So we have some free variables ($x_2, x_4$), and we want to solve for them. That's pretty easy, just solve each of them for terms of the others and show when they are free.
	- $x_1 = 3x_2 - 4x_4$
	- $x_2 = free$
	- $x_3 = 7x_4 - 1$
	- $x_4 = free$
	- $x_5 = 4$
- So with this, we've parameterized the solutions such that they will always be true for any given value of $x_2$ or $x_4$. Free variables can also be called free parameters, or just parameters.