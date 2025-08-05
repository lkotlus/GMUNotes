## Introduction
- Computers exist because of digital circuits.
- Mainly digital circuits that employ the use of logic gates. These are called logic circuits. 
- These use binary logic.
- We will be discussing how these work, and how they are described mathematically (Boolean Algebra, baby).

### 2.1 - Variables and Functions
- Binary circuits are great because of their simplicity. There's only two options for everything!
- The simplest binary component is that of a switch.
	- We'll control it with the variable $x$.
	- The switch allows current to flow when $x=1$
	- The switch blocks current when $x=0$
- If we attach a light bulb to our circuit, then we will find that the state of the light is equal to the state of $x$. We could denote the light as $L$ and say that $L(x)=x$.
- This logic expression describes a logic function, $L(x)$ and a logic variable, $x$.
- With two switches in series, we need both to be on. We would describe this as $L(x_1,x_2)=x_1\land x_2$ ("$x_1$ and $x_2$").
	- Boolean algebra in this class, so "and" is multiplication
	- $L(x_1, x_2)=x_1\cdot x_2$
- With two switches in parallel, just one variable needs to close the switch, therefore $L(x_1, x_2)=x_1+x_2$
- Get super crazy and add a switch in series with the two switches in parallel, and you get $L(x_1, x_2, x_3)=(x_1+x_2)\cdot x_3$ (if you're a Boolean Algebro)

### 2.2 - Inversion
- I mean, I don't not want to learn about this.
- $L(x)=\overline{x}$ ("$L(x)$ is equal to not $x$")
- This is also known as the complement operation. The complement of a function is shown as: $$f(x_1,x_2)=x_1+x_2$$ $$\overline{f}(x_1,x_2)=\overline{x_1+x_2}$$

### 2.3 - Truth Tables
- We have an expression, we want to see the output for each input. Easy: $$f(x_1,x_2,x_3)=x_1\cdot x_2\cdot x_3$$

|$x_1$, $x_2$, $x_3$|   $f(x_1,x_2,x_3)$   |
|---------------------|------------------|
|0,0,0|0|
|1,0,0|0|
|1,1,0|0|
|1,0,1|0|
|1,1,1|1|
|0,1,0|0|
|0,1,1|0|
|0,0,1|0|


### 2.4 - Logic Gates and Networks
- Each logic operation can be created with transistors and electronically implemented as logic gates.
- We can put these together in circuit diagrams, which we call schematics.
- A network of logic gates is called a logic network, or simply a logic circuit. These are interchangeable terms.
#### Analysis of a Logic network
- We can display a sequence of values for each bit in a circuit diagram, which results in what is called a timing diagram. This is essentially the same as a truth table.
- CAD tools frequently generate timing diagrams.
- Functionally equivalent networks:
	- Take the two networks: $$\overline{x}_1+x_1\cdot x_2$$ $$\overline{x}_1\cdot x_2$$
	- Upon inspection, they have identical truth tables. From this we can conclude that $$\overline{x}_1+x_1\cdot x_2=\overline{x}_1\cdot x_2$$
	- Very cool. We will soon learn how to simplify expressions to check if they are equal via Boolean Algebra!

### 2.4 - Boolean Algebra
- George Boole, my hero.
- Application for Boolean Algebra wasn't found until 100 years after it was invented!
- We have some axioms and theorems, they're all super easy.
- Duality:
	- A "dual" of a Boolean Algebra expression is when you replace all $1$ with $0$ and all $+$ with $\cdot$ and vice-versa.
	- The dual of any true statement is also true in Boolean Algebra (THIS IS CRAZY).
	- This can help us to simplify circuits!
- You're gonna need to work on memorizing some of the identities. Mostly just everything after DeMorgan.
	 $x\cdot y = y\cdot x$
	- $x+y=y+x$
	- $x\cdot(y\cdot z)=(x\cdot y)\cdot z$
	- $x+(y+z)=(x+y)+z$
	- $x\cdot(y+z)=x\cdot y+x\cdot z$
	- $x+y\cdot z=(x+y)\cdot(x+z)$
	- $x+x\cdot y=x$
	- $x\cdot(x+y)=x$
	- $x\cdot y+x\cdot\overline{y}=x$
	- $(x+y)\cdot(x+\overline{y})=x$
	- $\overline{x\cdot y}=\overline{x}+\overline{y}$
	- $\overline{x+y}=\overline{x}\cdot\overline{y}$
	- $x+\overline{x}\cdot y=x+y$
	- $x\cdot(\overline{x}+y)=x\cdot y$
	- $x\cdot y +y\cdot z+\overline{x}\cdot z=x\cdot y+\overline{x}\cdot z$
	- $(x+y)\cdot(y+z)\cdot(\overline{x}+z)=(x+y)\cdot(\overline{x}+z)$
- These are easily checked with a maximum of 8 scenarios. Proof by exhaustion is so easy in Boolean Algebra.
- Venn Diagrams
	- We can represent a shaded region as 1 and unshaded as 0.
	- We can then label shapes, and show where things are 1 and 0. This is an easy visualization of expressions.

### 2.6 - Synthesis Using AND, OR, and NOT Gates
- So we have established Boolean Algebra, circuit implementations of functions within it, and now we want to actually make things that are useful.
- Let's take the example of a function that monitors two bits: $x_1, x_2$. These two bits could be anything, but we want to output 1 when we have values $(0,0),(0,1),(1,1)$.
	- Reading aloud, we can literally see it as "0 and 0, 0 and 1, or 1 and 1".
	- This gives $\overline{x}_1\overline{x}_2+\overline{x}_1x_2+x_1x_2$
- We can simplify this all the way down to $x_2+\overline{x}_1$.
- The process of describing behavior and creating a circuit to implement it is called *synthesis*.
#### 2.6.1 - Sum-of-Products and Product-of-Sums Forms
- Pretty easy to explain. You have everything described as either sum of products (SoP) or a product of sums (PoS).
- Minterms:
	- A minterm of an $n$ variable function is a sum where each of the $n$ variables only appears once and produces a 1.
- Maxterms:
	- By duality, use OR instead of AND, and we get everything that produces a 0 in the function.

|Row|$x_1$|$x_2$|$x_3$|Minterm|Maxterm|
|-|-|-|-|-|-|
|0|0|0|0|$m_0=\overline{x}_1\overline{x}_2\overline{x}_3$|$M_0=x_1+x_2+x_3$|
|1|0|0|1|$m_1=\overline{x}_1\overline{x}_2x_3$|$M_1=x_1+x_2+\overline{x}_3$|
|2|0|1|0|$m_2=\overline{x}_1x_2\overline{x}_3$|$M_2=x_1+\overline{x}_2+x_3$|
|3|0|1|1|$m_3=\overline{x}_1x_2x_3$|$M_3=x_1+\overline{x}_2+\overline{x}_3$|
|4|1|0|0|$m_4=x_1\overline{x}_2\overline{x}_3$|$M_4=\overline{x}_1+x_2+x_3$|
|5|1|0|1|$m_5=x_1\overline{x}_2x_3$|$M_5=\overline{x}_1+x_2+\overline{x}_3$|
|6|1|1|0|$m_6=x_1x_2\overline{x}_3$|$M_6=\overline{x}_1+\overline{x}_2+x_3$|
|7|1|1|1|$m_7=x_1x_2x_3$|$M_7=\overline{x}_1+\overline{x}_2+\overline{x}_3$|

- So if you know which  things you want to produce as a 1, then your function is just the sum of the minterms or the product of the maxterms.
- For example, with the above if we want rows 0, 1, and 3 to produce a 1, then we can just say that $f=m_0+m_1+m_3=\sum m(0,1,3)$.
- We can also say that $f=M_0\cdot M_1\cdot M_3=\prod M(0,1,3)$.
- Easy enough. This is very important, so make sure you fully understand it.

### 2.7 - NAND and NOR Logic Networks
- Whenever we have something in PoS, we know that it can be implemented as an OR-AND network. For SoP, we know that it can be implemented as an AND-OR network. 
- It turns out that having something entirely made out of NAND and NOR circuits is faster, and we can convert OR-AND to NOR-NOR and AND-OR to NAND-NAND.
- The rules for this are simple:
	- Inversion becomes a double input from one variable into a NAND or NOR
	- AND-OR:
		- Change the AND gates to NAND gates, showing that their outputs get inverted again at the final OR
		- Change the final OR gate with all inverted inputs to a NAND gate with no inverted inputs, as they are equivalent.
	- OR-AND:
		- Change the OR gates to NOR gates, showing that their outputs get inverted again at the final AND.
		- Change the final AND gate with all inverted inputs to a NOR gate with no inverted inputs, as they are equivalent.

### 2.8 - Design Examples
- It's literally just examples of applications.

### 2.9 - Introduction to CAD Tools
- CAD helps us do stuff, we want to know how to use it.
- So we start with design entry, we manually start making things.
- Schematic Capture
	- A schematic capture tool is one that lets you draw a schematic.
	- Creating a circuit that is made up of smaller circuits is common, and referred to as hierarchical design.
	- This is good for smaller projects, but larger circuits will frequently become too much to handle.
- Hardware Description Language (HDL)
	- An HDL is similar to a programming language, but it is used to describe hardware rather than write code.
	- Imagine JSON but it creates a circuit diagram.
	- We use the IEEE standard in this course.
		- This includes Verilog HDL and the Very High Speed Integrated Circuit Hardware Description Language (VHDL). We use Verilog here.
- Logic Synthesis
	- We want to take either a circuit diagram or some Verilog code and make it faster. This is what our synthesis stuff does.
	- Boolean algebra.
	- As we compile Verilog code, optimizations are made.
- Functional Simulation
	- We can simulate how the circuit will perform. Duh.
- Physical Design
	- Shows us how we can implement our design on a physical chip.
- Timing Simulation
	- We want to observer propagation delay within a circuit. The effects of propagation delay are very important.
	- The timing simulator will allow us to do this.
- Circuit Implementation
	- Chip fabrication!
	- If we're using a programmable hardware device instead, then it's really chip configuration or chip programming.

### 2.10 - Introduction to Verilog
- When using CAD tools, we want to provide descriptions of our project with Verilog code.
- Structural Specifications of Logic Circuits:
	- We have gate-level primitives that are for commonly used gates.
	- `and (y, x1, x2);` (stores $x_1\cdot x_2$ in $y$)
	- `or (y, y1, x);` (stores $y_1+x$ in $y$)
	- `not (x, y);` (stores $\overline{y}$ in $x$)
	- We can use `nor` and `nand` as well.
	- Observe this incredible Verilog:
```verliog
module example1 (x1, x2, s, f);
	input x1, x2, s;
	output f;
	
	not (k, s);
	and (g, k, x1);
	and (h, s, x2);
	or (f, g, h);
endmodule
```
- Pretty self-explanatory. 
- We can skip not gates by using the `~` operator. 
- Behavioral Specification of a Logic Circuit
	- We can speed things up a lot by just saying `assign f = (~s & x1) | (s & x2);`. Just do Boolean Algebra.
	- We can also do if-else statements.
	- We support looping as well.
	- We can write modular code, which is always good.
- That's pretty much it to be honest. Fairly straightforward, but you need to practice.


### 2.11 - Minimization and Karnaugh Maps
- Don't you hate it when Boolean Algebra?
- We don't need to Boolean when Karnaugh maps Our Algebra.
- We can kind of tell how to do some things based on our truth tables, what if the truth tables were made to look more helpful for us?
- You can just change your truth table into a rectangle and figure it out from there. That's the whole thing.

### 2.14 - Incompletely Specified Functions
- Sometimes there's a condition that never happens. If we have inputs $x_1,x_2$ and know that the values will always be 00, 01, or 10, then we can call 11 a *don't care condition*, on account of the fact that we just don't care about it.
- A function that has such conditions are said to be incompletely specified.
- For minterm/maxterm notation: $$f(x_1,...,x_4)=\sum m(2, 4, 5, 6, 10)+D(12, 13, 14, 15)$$
- The above states that minterms 12, 13, 14, and 15 are don't care conditions. We can technically use them to simplify the function if it helps. It will count as either a 1 or 0, whatever is best for us. This works best on a Karnaugh Map.

### 2.15 - Multiple-Output Circuits
- Some circuits have multiple outputs. That just means we have two functions implemented.
- When this is the case, we just want to make sure that we use any available shared terms, because those can be recycled in the final circuit diagram.
- It's typically pretty easy to see things like this with a Karnaugh Map.