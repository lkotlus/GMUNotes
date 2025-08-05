### Basic administrative stuff
- We're using canvas, not blackboard
- Office hours are Tuesdays and Thursdays from 1-2. There will be another set with the TA, but it has not been announced yet.
- Grading
	- 20% homework
	- 20% in-class group work
	- 20% midterms 1 and 2
	- 20% final
	- 100% emotional damage (60% exam-based grades)
- In-class group work is either individual or as a small group of 2-3 people. It shouldn't take long and will be on Thursday classes (10-15 minutes). Paper and writing utensil is required, lowest three grades are dropped. Open book, open note, etc.
- Kept syllabus material to a minimum. Took 10 minutes. Chad.

## Linear algebra

### Section 1.1 - Systems of Linear Equations
- A bunch of definitions!
	- A **linear equation** is one in the form $a_1x_1 + a_2x_2 + ... + a_nx_n=b$. Everything in the form of $a_n$ is a constant, $x_n$ is a variable, and you are solving for a constant, $b$.
		- Example: $2x_1-3x_2=4$ is a linear equation of two variables.
		- Example: $x_1x_2-2x_3=7$ is not a linear equation! We are multiplying variables. We sum variable terms and multiply them by constants. That is all, no multiplication or exponents allowed.
	- A **system of linear equations** is a collection of linear equations in the same variables.
		- Example: $$\begin{array}{l}
		  2x_1-x_2+3x_3=7 \\
		  x_2+2x_3=-1
		  \end{array}$$
	- A **solution** to a system of equations in variables $x_1,...,x_n$ is a list of real numbers ($s_1...s_n$), where when $s_n$ corresponds to $x_n$, each equation is true when substituted for the variables.
		- Example: $$\begin{array}{l}
		  x_1-3x_2=7 \\
		  2x_2=4
		  \end{array}$$
		- The above has a solution of $(x_1,x_2) = (13,2)$.

#### Systems of 2 equations in 2 variables
- The nice thing about these is that we are able to graph them as lines. $2x_1-3x_2=7$ can be plotted in the $x_1$, $x_2$ plane. If we have a system of 2 equations in 2 variables, then we are able to create two lines within the same plane. They will intersect, be parallel, or be the same line (thus intersecting at all points).
- So we will have a unique solution, no solution, or an equation that generates infinitely many solutions. Legit.

#### Generalized
- The above fact is much more generalized.
- In general, a system of linear equations in any number of variables has:
	1. No solution
	2. A unique solution
	3. Or infinitely many solutions
- A system is **consistent** for scenarios 2 and 3 and **inconsistent** for scenario 1.

#### Matrix notation
- Let's take the given system of equations $$\begin{array}{l}
  -2x_1+3x_2-x_3=7 \\
  x_1-2x_3=0 \\
  x_1+7x_2+8x_3=0
  \end{array}$$
- From that, we can create a coefficient matrix: $$\begin{bmatrix}
  -2 & 3 & -1 \\
  1 & 0 & -2 \\
  1 & 7 & 8 \\
  \end{bmatrix}$$
- We can create a larger matrix that records what occurs on the right hand side of the system as well (called the augmented matrix): $$\begin{bmatrix}
  \,-2 & 3 & -1 & 7 \, \\
  1 & 0 & -2 & 4 \, \\
  1 & 7 & 8 & 0 \, \\
  \end{bmatrix}$$
- Matrices are always defined with a size given as $(\#rows)*(\#columns)$. So above, we have a 3x3 matrix as our coefficient matrix and a 3x4 matrix as our augmented matrix.

#### Solving a system of linear equations
- Idea:
	- Add/subtract multiples of the equations from one another until the answer can be found within the simpler system resulting form this process.
- Example:
	- Solve: $$\begin{bmatrix}
	  1 & -3 & 0 & 5 \, \\
	  -1 & 1 & 5 & 2 \, \\
	  0 & 1 & 1 & 0 \, \\
	  \end{bmatrix}$$
	- We have been given our augmented matrix, the rightmost row is our answers. We will begin by adding our first equation to the second. This results in: $$\begin{bmatrix}
	  1 & -3 & 0 & 5 \, \\
	  0 & -2 & 5 & 7 \, \\
	  0 & 1 & 1 & 0 \, \\
	  \end{bmatrix}$$
	  This simplifies our second equation, as it is now in just 2 variables.
	- Now, we can add equation 3 multiplied by 2 to equation 2. That will eliminate another element in equation 2 giving the value of $x_3$. This results in: $$\begin{bmatrix}
	  1 & -3 & 0 & 5 \, \\
	  0 & 0 & 7 & 7 \, \\
	  0 & 1 & 1 & 0 \, \\
	  \end{bmatrix}$$
	  It is easy to see from here that $x_3$ is equal to 1, because equation 2 has become $7x_3=7$.
	- We can even simplify our second equation within the matrix, giving: $$\begin{bmatrix}
	  1 & -3 & 0 & 5 \, \\
	  0 & 0 & 1 & 1 \, \\
	  0 & 1 & 1 & 0 \, \\
	  \end{bmatrix}$$
	- That makes the next step super easy to get to, subtracting equation 2 from equation 3: $$\begin{bmatrix}
	  1 & -3 & 0 & 5 \, \\
	  0 & 0 & 1 & 1 \, \\
	  0 & 1 & 0 & -1 \, \\
	  \end{bmatrix}$$
	  This gives that $x_2=-1$.
	- Very cool! Just add three times equation 3 to equation 1, giving: $$\begin{bmatrix}
	  1 & 0 & 0 & 2 \, \\
	  0 & 0 & 1 & 1 \, \\
	  0 & 1 & 0 & -1 \, \\
	  \end{bmatrix}$$
	  It's technically solved, but let's interchange 2 and 3 to make it look nice and pretty (something something algorithm, something something determinant): $$\begin{bmatrix}
	  1 & 0 & 0 & 2 \, \\
	  0 & 1 & 0 & -1 \, \\
	  0 & 0 & 1 & 1 \, \\
	  \end{bmatrix}$$
	- All in all, we have $(x_1,x_2,x_3)=(2,-1,1)$ as the unique solution to this system of equations.
- The three kinds of operations we can do when solving by elimination like this (**Elementary Row Operations**):
	1. Replace a row by the sum of itself and the multiple of another row.
	2. Interchange two rows, changing the order.
	3. Multiply all entries in a row by a nonzero constant.
- These operations are reversible!
- Two systems that are related by a sequence of elementary row operations are called **row equivalent**, and they have the same set of solutions.
- Homework is due **next** Friday (September 6). Get logged in on MyLab.

# Example that I shall solve at home
$$\begin{bmatrix}
  0 & 1 & -4 & 8 \, \\
  2 & -3 & 2 & 1 \, \\
  4 & -8 & 12 & 1 \, \\
\end{bmatrix}$$