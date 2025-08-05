### Warm up
- We saw that the rate of change equation $\frac{dP}{dt}=0.3P$ can be used to model a situation where there is one species. 
- In most situations, however, resources are not unlimited. In what ways does the modified rate of change equation $\frac{dP}{dt}=0.3P(1-\frac{P}{10})$ account for limited resources?
	- We can see that rate of change in the population will decline after it reaches a certain threshold. If $P>10$, then rate of change will be 0, and if it is greater, then rate of change will be negative. 
	- We will experience exponential growth that tapers off as the population grows to surpass the available resources.
- Side notes:
	- We initially see exponential growth because it's just multiplying the equation by 1.
	- If the initial population is 20, we see the exponential being multiplied by negative 1.
- How do you interpret the solution with initial condition $P(0)=10$?
	- Equilibrium.
- <u>**Definition**</u>: An Equilibrium Solution is a constant function that satisfies the DE.
	- How many equilibrium solutions are there for the DE above? What are they?
		- 2, and they are $P=0$ and $P=10$
	- We can do this by just finding the roots where $\frac{dP}{dt}=0$.

### Class outline
- Numerical approach:
	- Algorithm for approximating solutions to any DE.
- Review:
	- What is a DE?
	- Finding functions that satisfy DEs
- Hinted at some approaches:
	- Graphical
	- Analytical
	- Numerical

### Numerical approach
- Slope field viewers let us observe what a slope filed looks like for a DE. Taking our DE from earlier, all of the analytical observations we have hold true graphically.
- If there are initially $P(0)=2$ fish in the lake, approximately how many fish are in the lake at time $t=2$? How did you arrive at your approximation?
	- So let's just follow the tangent lines along small increments. So initially, we have $P-2=0.48(t-0)$, which gives $P=0.48t+2$. Follow that line to the next value, and repeat until you reach $t=2$.