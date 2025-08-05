### Midterm Statistics
- Van, the GOAT, got a 100
	- I, not the GOAT, got a 93
- "So the class averages was pretty low"
	- 73.9
- That means I get an A+
- 20% of the class got over 90
- Median is 72

### Arithmetic Circuits
- We increase the RCA circuit with CLA (Carry Lookahead Adder). It provides a significant increase in speed at the cost of additional hardware.
- Looking at performance in circuits is mainly done with critical-path-delay. Essentially, look at the worst case scenario.
- CLA seeks to reduce the critical-path-delay, which is our bottleneck in RCA.
- So we want to have a variable called "carry generate", which creates "carry end". So essentially, see when the carry starts and bring it to when the carry finishes. We also have carry propagate along each point where the carry continues.
- Carry is generated if $AB$. Carry is propagated if $A+B$ (alternatively $A\oplus B$).
- So carry-out is realized as:
	- $c_{i+1}=x_iy_i+x_ic_i+y_ic_i$
- Or...
	- $c_{i+1}=x_iy_i+(x_i+y_i)c_i$
- We can just say that $g_i=x_iy_i$ (generate), $p_i=x_i+y_i$ (propagate), and this results in $c_{i+1}=g_i+p_ic_i$.
- RCA has $2n+1$ delays for an $n$-bit implementation in the critical-path (just count the amount of gates it takes to get all the carry bits).
- CLA improves this by running $c_0$ throughout the whole circuit. In total for an $n$-bit CLA, we have 4 gate delays. All $g_i$ and $p_i$ are one delay, all $c_i$ is two more, and there's one more for the sums $s_i$.
- Fan-in limitations can create performance issues, and CLA circuits can get very complex. We can reduce complexity with hierarchical design. 
	- For a 32 bit adder, divide the adder into 4 8-bit adders.
	- This creates RCA delay all over again. To get around this we use second level CLA.
	- For second level CLA, $P_0=p_7p_6...p_1p_0$, $G_0=g_7+p_7g_6+p_7p_6g_5+...+p_7p_6p_5p_4p_3p_2p_1g_0$
	- There's more here. You need to read the textbook.
- Rather than needing to implement these, the professor will focus on the differences between the two. For the final I need to be able to compare the differences in path time for the two.