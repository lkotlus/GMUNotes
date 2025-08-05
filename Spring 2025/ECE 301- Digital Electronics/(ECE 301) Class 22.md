### Registers
- A flip-flop stores one bit of information
- When a set of $n$ flip-flops is used to store $n$ bits of data, we refer to these flip-flops as a *register*
- Normal registers all have their own inputs and outputs that are separate. Typically we do this with D flip flops, and sometimes we have a load trigger.
- Shift registers are just a bunch of D flip flops in series. It's just a bit shift each clock signal. 1000 -> 0100 -> ...
- Parallel-access shift registers are crazy
	- So we have a serial input and output, duh.
	- We have $\overline{\text{shift}}/\text{load}$. When this is 1, parallel inputs are loaded to the registers. When 0, we operate as a shift register.
	- Other than that, we just have the clock.
	- So essentially, when load is 1 we set each flip flop to the values specified. When load is 0, we're a shift register.
	- This makes sense.
	- We can implement this with 4-1 MUX. That's 2 inputs for 4 potential outputs. Neat.
- Counters
	- Special purpose arithmetic circuits used for the purpose of counting
		- Design circuits that can increment or decrement a count by 1
	- Counter circuits serve many purposes:
		- Count occurrences of certain events
		- Generate timing intervals for controlling various tasks in a digital system
		- Track elapsed time between events
	- Often (but not always) built with T flip-flops because the toggle feature is naturally suited for implementing the counting operation.
	- This is the easiest method. We just have all the T flip flops with active T. We view the output $Q$ for our counter digits, and $\overline{Q}_n$ feeds into $\text{CLK}_{n+1}$. 
		- Highly elegant solution.
		- This counts up
	- To count down we can do the same thing, but $Q_n$ feeds into $\text{CLK}_{n+1}$.
	- We can make synchronous counters, that is, counters that all use the same clock signal. This requires AND gates.
	- We can add in enable and clear signals as well.
	- Counters can be implemented with D flip-flops as well.
		- We can even create parallel load counters this way

### Designing with System Requirements
- So if we have system requirements, we should be able to design a circuit that implements it.
- For example, give me a modulo-6 counter:
	- 000
	- 001
	- 010
	- 011
	- 100
	- 101
	- 000
	- ...
- Designing this has seven easy steps:
	1. Draw a state diagram
	2. Construct a state table from the state diagram
		- One flip-flop is required for each state bit
	3. Select the type of flip-flop to be used in the counter design
	4. Use FF Excitation Table to determine flip-flop input values
	5. Construct the K-map for each flip-flop input
		- FF inputs are each a function of the present state of the counter
	6. Derive the minimum Boolean expression for each flip-flop input
	7. Draw the circuit diagram for the counter
		- Include the proper number of flip-flops
		- Use logic gates to realize teh Boolean expressions
- Seven "easy" steps...
- Design a counter circuit to meet the following specifications:
	- 3 bit UP counter
	- Uses $D$ flip-flops to store the state of the counter
	- Uses a minimum number of logic gates
	- Let's go through the steps:
		1. Draw the state graph:
			- 000 -> 001 -> 010 -> 011 -> 100 -> 101 -> 110 -> 111 -> 000 -> ...
		2. Construct the state table
			- |$Q_2$|$Q_1$|$Q_0$|$Q_2^+$|$Q_1^+$|$Q_0^+$|
			  |-|-|-|-|-|-|
			  |0|0|0|0|0|1|
			  |0|0|1|0|1|0|
			  |0|1|0|0|1|1|
			  |0|1|1|1|0|0|
			  |1|0|0|1|0|1|
			  |1|0|1|1|1|0|
			  |1|1|0|1|1|1|
		3. Select the FF type (given, $D$)
		4. Use the excitation table to determine flip flop input values
			- Well, we know that $D_n=Q_n^+$
		5. Construct the K-map for each flip-flop input
			- For this we just make a K-map for each $D$ in terms of $Q_0$ through $Q_n$
		6. Get it in Boolean Algebra
			- Big ole' Boolean expression
		7. Make a circuit diagram!