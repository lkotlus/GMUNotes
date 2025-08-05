### Warm up
- Use the chain rule to write down, symbolically, the derivative with respect to $t$ of $\ln (P)$:
	- $\frac{d}{dt}\left[\ln(P)\right]=\frac{1}{P}\cdot\frac{dP}{dt}$

### Analytic approach
- **<u>Finally</u>**
- Example:
	- Tom and Jerry both want to get the population of a species after 2.5 years. The differential equation is: $$\frac{dP}{dt}=0.2P$$
	- So Tom uses Euler's method, and Jerry will make a continuous graph.
	- How are they different? Will they get the same predictions?
		- They're different because one has segments of rate of change and the other is literally the function that solves the equation.
	- They will be identical for $P(0)=0$.
	- Tip to tail graph will be less than the continuous one.
- So Jerry has an analytical approach, and that gives us an exact solution! That's what we want to do. For what Jerry did:
	- Firstly, divide both sides by $P$: $$\frac{1}{P}\frac{dP}{dt}=0.2$$
	- Afterwards, multiply both sides by $dt$: $$\frac{1}{P}\ dP=0.2\ dt$$
	- Now we can integrate both sides: $$\int\frac{1}{P}\ dP=\int0.2\ dt$$
	- Assuming that $P>0$, this gives us that $$\ln(P)=0.2t+C$$
	- Neat, now let's get $P$ alone: $$P=e^{0.2t+C}$$ $$P=e^Ce^{0.2t}$$ $$P=ke^{0.2t}$$
	- $P(0)=2$ (perchance), so the equation Jerry had is $P=2e^{0.2t}$.
- Definitions:
	- <u>General Solution</u>:
		- Solution to a DE that represents all possible functions that satisfy the DE.
	- <u>Particular Solution</u>:
		- A single solution that satisfies the DE.
	- <u>Separable Differential Equation</u>:
		- An equation where we can separate variables and integrate.
	- <u>Separation of Variables</u>:
		- Separating the variables...