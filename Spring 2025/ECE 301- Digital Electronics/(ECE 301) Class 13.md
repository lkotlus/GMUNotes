### Addition and Subtraction Continued
- So recall that single bit addition and subtraction have the same basic truth table when ignoring carry and borrow bits:

|$A$|$B$|Carry|Sum|Difference|
|-|-|-|-|-|
|0|0|0|0|0|
|0|1|0|1|1|
|1|0|0|1|1|
|1|1|1|0|0|

- Notice that carry is an AND gate and sum/difference are both an XOR gate.
- For the case $0-1$ in difference, we require a borrow bit.
- Unsigned numbers just use every bit for MSB through LSB. This is good for larger numbers, but we can't do negative numbers!
- Signed numbers move the MSB back by one and uses $d_{n-1}$ to denote the sign of the number. $0$ is positive, $1$ is negative.
	- We still have the same number of combinations, and so we can still represent $2^n$ numbers.
- So we need a carry and sum bit for signed addition, and that's it! This is called a half adder (HA).

|$A$|$B$|Carry|Sum|
|-|-|-|-|
|0|0|0|0|
|0|1|0|1|
|1|0|0|1|
|1|1|1|0|

- The full adder circuit requires the carry bit to be considered from the previous addition!

|$c_i$|$x_i$|$y_i$|$c_{i+1}$|$s_i$|
|-|-|-|-|-|
|0|0|0|0|0|
|0|0|1|0|1|
|0|1|0|0|1|
|0|1|1|1|0|
|1|0|0|0|1|
|1|0|1|1|0|
|1|1|0|1|0|
|1|1|1|1|1|

- This is synthesized to $s_i=c_i\oplus x_i\oplus y_i$ and $c_{i+1}=x_iy_i+x_ic_i+y_ic_i$.
- We really have two HA circuits joined together here. 
- We really just need a bunch of full adder circuits in sequence leading into one another. This is called a ripple adder.
- $n$-bit addition requires an $n$ depth ripple carry adder (RCA) circuit.

### Midterm Review
- 2.5 hours, we get to have a calculator.
- Lockdown browser :(
- Priority things to study:
	- All lecture slides and in-class examples
	- Homework problems
	- All problems will be multiple choice, there will be 14 problems (each problem is weighted the same)
	- One page cheat sheet
	- All problems will be quantitative, we solve them for answers. No essay, definition, true/false, or anything like that. We are doing practical applications. Epic.
	- Big skills to have:
		- K-maps for both SOP and POS
		- Conversion from POS to SOP, minterm/maxterm notation, etc.
		- Binary to decimal and decimal to binary conversions
		- Designing circuits/logic synthesis from a word problem
		- Finding a circuit in boolean algebra, a circuit diagram, a truth table, a timing diagram, etc.
		- Boolean algebra (technically, but mainly use K-map)
		- Cost analysis (count <u>***EVERYTHING***</u>, even inverters and inputs to them, we won't need to do cost for NOR and NAND)