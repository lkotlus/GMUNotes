### Starting off With Some Examples
- Construct a truth table for the following Boolean expressions:
	- $\text{F}(A,B,C)=(\overline{A}+B)(\overline{B}+\overline{C})(A+B+C)$
	- $\text{F}(A,B,C,D)=\overline{B}CD+A\overline{D}+\overline{A}BD+A\overline{B}\overline{C}D$
- This is pretty easy.

|$A$|$B$|$C$|$F$|
|-|-|-|-|
|0|0|0|0|
|0|0|1|1|
|0|1|0|1|
|0|1|1|0|
|1|0|0|0|
|1|0|1|0|
|1|1|0|1|
|1|1|1|0|

|$A$|$B$|$C$|$D$|$F$|
|-|-|-|-|-|
|0|0|0|0|0|
|0|0|0|1|0|
|0|0|1|0|0|
|0|0|1|1|1|
|0|1|0|0|0|
|0|1|0|1|1|
|0|1|1|0|0|
|0|1|1|1|1|
|1|0|0|0|1|
|1|0|0|1|1|
|1|0|1|0|1|
|1|0|1|1|1|
|1|1|0|0|1|
|1|1|0|1|0|
|1|1|1|0|1|
|1|1|1|1|1|

- Note that SoP is a lot easier. We can just fill in each thing that causes a single part of the expression to be a 1. Much easier.
- With SoP we can also read minterms off the truth table to get a Boolean expression. Super neat.
- If we have some function $\text{F}$, we can find $\overline{\text{F}}$ very easily if it's in either SoP or PoS. You will end up with a function in the opposite form by DeMorgan's.
- If we want to go from truth table to PoS, just read off the maxterms on your 0 rows.
- The problem with Boolean Algebra is that we just don't know when an expression is fully simplified.
- Karnaugh Maps give us a better way to do this. We will discuss these later.

### Standard Forms
- So our standard forms are SoP and PoS.
- Pretty easy. SoP is the best, PoS is a gigantic pain.
- Question:
	- Design a logic circuit with three inputs: $x,y,z$. The circuit output should be 1 only when $x=1$ and $y=1$ or $z=1$ or both.
	- So from the truth table below, we can see that: $$f(x,y,z)=x\overline{y}z+xy\overline{z}+x\overline{y}\overline{z}=x(y+z)$$

|$x$|$y$|$z$|$f$|
|-|-|-|-|
|0|0|0|0|
|0|0|1|0|
|0|1|0|0|
|0|1|1|0|
|1|0|0|0|
|1|0|1|1|
|1|1|0|1|
|1|1|1|1|

### Logic Synthesis
- So we have our minterms and our maxterms. Epic.
- we can do things with NAND-NAND and NOR-NOR as well as our AND-OR/OR-AND. we'll stick for the latter two for now.