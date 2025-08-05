### Solution sets of linear systems
- We can write a system in matrix form...
$$
A\overrightarrow{x}=\overrightarrow{b}
$$
- $A$ is some $m\text{x}n$ matrix.
- If $\overrightarrow{b}=\overrightarrow{0}$, then the system is called homogeneous. It always has a solution.
	- $A\overrightarrow{x}=\overrightarrow{0}$
- Homogeneous systems are always consistent as they always have a solution. The solution $\overrightarrow{x}=\overrightarrow{0}$ is called the **trivial solution** because it is the one always present in homogeneous systems. The system could have more solutions, which would be called **non-trivial solutions**.
- Example!
	- So take the system:$$
x_1 + 2x_2 - x_3 = 0
x_2 + x_3 = 0$$
	- We know that this is really just:$$\overrightarrow{x}=\begin{bmatrix}x_1\\x_2\\x_3\end{bmatrix}$$$$
\overrightarrow{b}=\overrightarrow{0}$$$$
A=\begin{bmatrix}1 & -2 & -1\\0 & 1 & 1\end{bmatrix}$$
	- Let's row reduce $A$.$$A=\begin{bmatrix}1 & 0 & 1\\0 & 1 & 1\end{bmatrix}$$
	- Alright, so we know that $x_3$ is our free variable. Let's just get our solutions in a familiar form:
		- $x_1=-x_3$
		- $x_2=-x_3$
		- $x_3=\text{free}$
	- We can also write it in this new way as a vector!$$
\overrightarrow{x}=\begin{bmatrix}x_1\\x_2\\x_3\end{bmatrix}=\begin{bmatrix}-x_3\\-x_3\\x_3\end{bmatrix}$$
	- Furthermore, we can factor $x_3$ out of our solution vector.$$
\overrightarrow{x}=\begin{bmatrix}x_1\\x_2\\x_3\end{bmatrix}=x_3\begin{bmatrix}-1\\-1\\1\end{bmatrix}$$
	- This tells us that our set of solutions is all scalar multiples of the vector $\begin{bmatrix}-1\\-1\\1\end{bmatrix}$. We also know that this is $\text{Span}\bigg\{\begin{bmatrix}-1\\-1\\1\end{bmatrix}\bigg\}$, which is a line in $\mathbb{R}^3$ that passes through $\overrightarrow{0}$.
- Very cool stuff 
- Let's look at the end of another example:
	- Our set of solutions is:$$
\overrightarrow{x}=\begin{bmatrix}x_1\\x_2\\x_3\end{bmatrix}=\begin{bmatrix}3x_2-x_3\\x_2\\x_3\end{bmatrix}$$
	- We can change this into an addition of two vectors...$$
\overrightarrow{x}=\begin{bmatrix}x_1\\x_2\\x_3\end{bmatrix}=\begin{bmatrix}3x_2\\x_2\\0\end{bmatrix} + \begin{bmatrix}-x_3\\0\\x_3\end{bmatrix}$$
	- We can see from this that we should factor things out, so...$$
\overrightarrow{x}=\begin{bmatrix}x_1\\x_2\\x_3\end{bmatrix}=x_2\begin{bmatrix}3\\1\\0\end{bmatrix} + x_3\begin{bmatrix}-1\\0\\1\end{bmatrix}$$
	- Which tells us that our solutions are contained in the set $\text{Span}\bigg\{\begin{bmatrix}3\\1\\0\end{bmatrix}, \begin{bmatrix}-1\\0\\1\end{bmatrix}\bigg\}$. This is a two-dimensional plane in $\mathbb{R}^3$ that passes through $\overrightarrow{0}$.
- But what about a system that isn't homogeneous? A heterogeneous system? Hell nah. That's an inhomogeneous/nonhomogeneous/general system.
- Well, the answer is that there might be no solutions, but if there are solutions we could be able to describe them geometrically.
- Example time!
	- So we have the following system:$$
A=\begin{bmatrix}1&0&-2\\0&1&1\end{bmatrix}$$$$
\overrightarrow{x}=\begin{bmatrix}x_1\\x_2\\x_3\end{bmatrix}$$$$
\overrightarrow{b}=\begin{bmatrix}1\\2\end{bmatrix}$$
	- Well, we're already in RREF, so let's just show our solutions:$$
\overrightarrow{x}=\begin{bmatrix}x_1\\x_2\\x_3\end{bmatrix}=\begin{bmatrix}1+2x_2\\2-x_3\\x_3\end{bmatrix}=\begin{bmatrix}1\\2\\0\end{bmatrix}+x_3\begin{bmatrix}2\\-1\\1\end{bmatrix}$$
	- Pretty neat. So we have solutions, which is good. Our result is a vector added to all scalar multiples of another vector. Let's generalize this as $\overrightarrow{x}=\overrightarrow{p}+x_3\overrightarrow{v}$. This means we just have a line in $\mathbb{R}^3$ that passes through $\overrightarrow{p}$. By passes through, we mean it just touches the point at the tip of $\overrightarrow{p}$. 
	- When we do that, $\overrightarrow{p}$ is called a particular point on the line and $\overrightarrow{v}$ is called the direction vector of the line.
	- **Theorem!**
		- If you look closely, you can see that if $A\overrightarrow{x}=\overrightarrow{b}$ is consistent and $\overrightarrow{p}$ is one particular solution, then any other solution is of the form $\overrightarrow{x}=\overrightarrow{p}+\overrightarrow{v}_h$ where $\overrightarrow{v}_h$ is a solution of the homogeneous system $A\overrightarrow{x}=\overrightarrow{0}$. 
	- Essentially, when we don't have a homogeneous system, the solution is just the solution to the equivalent homogeneous system shifted over by some vector. The solution set is either empty, or looks like the span of some vectors translated by any particular solution.
	- Let's do another example.
		- So take our system:$$
A = \begin{bmatrix}1&-3&1\end{bmatrix}$$$$
\overrightarrow{x}=\begin{bmatrix}x_1\\x_2\\x_3\end{bmatrix}$$$$
\overrightarrow{b}=\begin{bmatrix}1\end{bmatrix}$$
	- Well, we've seen before that the general solution to this is:$$
\overrightarrow{v}_h=\begin{bmatrix}x_1\\x_2\\x_3\end{bmatrix}=x_2\begin{bmatrix}3\\1\\0\end{bmatrix} + x_3\begin{bmatrix}-1\\0\\1\end{bmatrix}$$
	- We need a single particular solution for this to get the full solution. $\overrightarrow{p}=\begin{bmatrix}0\\-\frac{1}{3}\\0\end{bmatrix}$ should work.
	- With this, we know that our full solution is just:$$
\overrightarrow{x}=\begin{bmatrix}0\\-\frac{1}{3}\\0\end{bmatrix}+x_2\begin{bmatrix}3\\1\\0\end{bmatrix} + x_3\begin{bmatrix}-1\\0\\1\end{bmatrix}$$
	- This is just a plane that includes the point $(0, -\frac{1}{3}, 0)$. Note that any point within the plane will work, because any valid particular solution for the system will work! Epic.

### Low dimensions
- Let's say we have two variables and two equations.
	- This means we have two lines in $\mathbb{R}^2$.
	- They can be parallel (no solutions)
	- They can intersect (unique solution, $\{\overrightarrow{p}\}$)
	- They can lie on top of one another (infinitely many solutions)
- Let's say we have three variables and three equations.
	- This means we have three planes in $\mathbb{R}^3$.
	- The planes can all intersect at one point (unique solution, $\{\overrightarrow{p}\}$)
	- The planes are all parallel (no solutions)
	- Planes could cross in pairs (no solutions)
	- Two parallel with one intersecting both (no solutions)
	- Planes could intersect to make a line (set of solutions, $\overrightarrow{p}+t\overrightarrow{v}$)
	- They're all the same plane ($\overrightarrow{p}+t\overrightarrow{v}+s\overrightarrow{w}$)