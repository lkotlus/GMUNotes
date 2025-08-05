## Chapter 2, Lecture 1
### Random Experiment
- An experiment is a procedure that is:
	- Carried out under controlled conditions
	- Executed to discover an unknown result
- A random experiment:
	- An experiment that can result in different outcomes, even though it is repeated int he same manner every time.

### Sample Spaces
- The set of all possible outcomes of a random experiment is called teh sample space, $S$.
	- Discrete: consists of finite or countable outcomes
	- Continuous: an interval of real numbers
- Examples (exam topic):
	- $S=R^+=\{x|x>0\}$ is continuous
	- $S=\{1.5<x<5\}$ is continuous
	- $S=\{\text{low}, \text{medium}, \text{high}\}$ is discrete
	- Does the camera conform to minimum recycle time specifications?
		- This means that $S=\{\text{yes}, \text{no}\}$, which is discrete
- Tree diagrams:
	- Describe sample spaces graphically
	- Sample can be constructed in several steps/stages, we can represent each of the $n_1$ ways of completing the first step as a branch of a tree
	- Each of the ways of completing the second step can be represented as $n_2$ branches starting from the ends of the original branches, and so forth.
	- Example:
		- Messages are either on-time or late. The tree diagram for an experiment with three messages is essentially just a binary tree with paths for on-time and late. 
		- It shows us the orders of the experiment.

### Events
- An event is a subset of the sample space of a random experiment.
- Event combinations:
	- The union of two events consists of all outcomes that are contained in either of the two events: $E_1\cup E_2$
	- The intersection of two events consists of all outcomes that are contained in both of the two events: $E_1\cap E_2$
	- The complement of an event in a sample space is the set of outcomes in the sample space that are not in the event. We denote the complement of the event $E$ as $E'$.
- Examples:
	- Sample space: $S=\{yy,yn,ny,nn\}$
	- Suppose that the subset of outcomes is denoted as $E_1=\{yy,yn,ny\}$.
	- Suppose that another is denoted as $E_2=\{nn\}$.
	- Other examples of events are $E_3=\varnothing$.
	- $E_1\cup E_2=\{yy,yn,ny,nn\}$
	- $E_2\cap E_3=\varnothing$
	- ...
- Events are used to define outcomes of interest from a random experiment. One is often interested in the probabilities of specified events.
- Venn diagrams can be used for events.
- Mutually exclusive events: $$E_1\cup E_2=\varnothing$$
- Some laws:
	- Double complement: $$(E')'=E$$
	- Distributive: $$(A\cup B)\cap C=(A\cap C)\cup(B\cap C)$$ $$(A\cap B)\cup C=(A\cup C)\cap(B\cup C)$$
	- DeMorgan's: $$(A\cup B)'=A'\cap B'$$ $$(A\cap B)'=A'\cup B'$$
	- Commutative: $$A\cup B = B\cup A$$ $$A\cap B = B\cap A$$
- Gaming

### Counting Techniques
- Determining the outcomes in the sample space (or an event) can become more difficult
- In these cases, counts of the numbers of outcomes in the sample spaces and various events are used to analyze the random experiments
- These methods are referred to as counting techniques:
	- Multiplication rule
	- Permutations
	- Combinations

#### Multiplication Rule
- Assume an operation can be described as a sequence of $k$ steps, and:
	- The number of ways to complete step 1 is $n_1$, step 2 is $n_2$, step 3 is $n_3$, ...
- The total number of ways to complete the operation is $\prod_{i=0}^k n_i$
- Example:
	- A website is supposed to consist of four colors, three fonts, and three positions for an image. There are $(4)(3)(3)=36$ outcomes.

#### Permutations
- A permutation of elements is an ordered sequence of the elements.
- $S=\{a,b,c\}$ has permutations $abc, acb, bac, bca, cab, cba$
- The number of permutations of $n$ different elements is $n!$
- Subsets: 
	- The number of permutations of subsets of $r$ elements selected from a set of $n$ elements is: $$P_r^n=\frac{n!}{(n-r)!}$$
	- Example:
		- A PCB has eight different locations in which a component can be placed. If four different components are to be placed on the board, how many different designs are possible? $$P_4^8=\frac{8!}{4!}=1{,}680$$
- Permutations of similar objects:
	- The number of permutations of $n=n_1+...+n_r$ objects where $n_1$ is one type of object, $n_2$ is another, and so on is: $$\frac{n!}{\prod_{i=0}^r(n_i!)}$$
	- Example:
		- A hospital operating room needs to schedule three knee surgeries and two hip surgeries in one day. We denote a knee surgery as $k$ and hip surgery as $h$. The number of possible sequences of three knee and hip surgeries is: $$\frac{5!}{(3!)(2!)}=\frac{120}{12}=10$$

#### Combinations
- The number of combinations, subsets of $r$ elements that can be selected from a set of $n$ elements, is denoted as $\begin{pmatrix}n\\r\end{pmatrix}$ or $C_r^n$: $$C_r^n=\begin{pmatrix}n\\r\end{pmatrix}=\frac{n!}{r!(n-r)!}$$
- In combinations, order is not important.
- Every subset of $r$ elements can be indicated by listing the elements in the set and marking each element with a "\*" if it is to be included in the subset
- Therefore, each permutation of r\*s and n-r blanks indicates a different subset
- For example, if the set is $S=\{1,2,3,4\}$, the subset $\{2,4\}$ can be indicated as: 
	- 1 2 3 4
	- -\*----*
- Example:
	- A bin of 50 parts contains 3 defectives and 47 non-defective parts. A sample of 6 parts is selected from the 50 without replacement. How many samples of size 6 contain 2 defective parts?
	- We have $n=3$ defective parts. We want $r=2$ defective parts, so: $$\frac{3!}{2!\cdot1!}=\frac{6}{2}=3$$
	- If the defective parts are $\{a,b,c\}$, then $ab$, $bc$, $ac$
	- Of the remaining four parts from the 47 acceptable parts in the bin, how many ways can the second step be completed?
	- We have $n=47$ working parts and want $r=4$, so: $$\frac{47!}{4!\cdot43!}=178{,}365$$
	- By the multiplication rule, we have: $$3\cdot 178{,}365=535{,}095$$