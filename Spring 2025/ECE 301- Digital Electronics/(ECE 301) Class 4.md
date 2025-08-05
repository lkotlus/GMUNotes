### Boolean Algebra
- Correctly guessed the topic of the day.
- Boolean (or switching) Algebra can be used to:
	1. Simplify complex Boolean expressions
	2. Manipulate (or change the form of) Boolean expressions
	3. Prove the equivalency of two Boolean expressions
- Problems with Boolean Algebra:
	- There isn't a set way to fully simplify something.
	- There isn't an easy way to know when something is fully simplified.
	- A better tool for simplifying Boolean expressions is the <u>Karnaugh Map</u> (K-map, discussed later).
- Our ultimate goal with Boolean Algebra is to simplify things and gain better performance.
- We have our axioms in the reading notes.
- Single variable theorems and multi-variable theorems are in reading notes as well.
- Duality! We swap $0$ for $1$ and $+$ for $\cdot$ and vice-versa for all expressions and constants within an expression. If you do this to a true expression, the result is another true expression!
- Algebraic manipulation can be used to simplify Boolean expressions.
	- Simpler expression -> simpler circuit
- It isn't practical to deal with complex expressions this way, so CAD tools do it for us. To understand how to use CAD better, we need to understand the fundamentals.
- Venn diagrams are sometimes used to show Boolean expressions.
- When you can choose between sum of products and product of sums, always go with sum of products as it is easier. They are duals of one another, so they will both work. 
- Always go NOT, AND, OR ($\overline{}, \cdot, +$) for your order of operations.
- When you have a product of sums, you can get the $1$ lines of your truth table from each product! $\overline{A}\cdot B\cdot C+A\cdot B\cdot\overline{C}+\overline{A}\cdot\overline{B}\cdot C$ clearly shows that we are true for $011$, $110$, and $001$.