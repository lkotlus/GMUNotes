### Recall Nullclines
- Isoclines are lines along which vectors have the same slope.
- We have $x$-nullclines are lines along which $\frac{dx}{dt}=0$, and $y$-nullclines are lines along which $\frac{dy}{dt}=0$. 
- If we look at the nullclines and how they interact at their intersections we can observe a lot about the behavior of the system.
- Equilibrium solutions are always when opposite nullclines meet. If $x$-nullclines intersect, it isn't equilibrium. 

### Starting on Solving Systems of DEs
- Warm up:
	- Use Newton's Law of Motion $\sum \overrightarrow{F}=m\overrightarrow{a}$, develop a rate of change equation to model the motion of an object on a spring. Assume that the only forces acting on the object are the spring force ($-kx$, $k$ is the spring constant and $x$ is displacement) and the friction force (assumed to be proportional to the velocity, namely $-b\frac{dx}{dt}$, where $b$ is the damping coefficient).
	- $\frac{dF}{dt}=\text{change in spring force} + \text{change in friction force}$
	- $\text{spring force}=-kx$
	- $\text{friction force}=-b\frac{dx}{dt}$
	- $\frac{dF}{dt}=-k\frac{dx}{dt}-b\frac{d^2x}{dt^2}$, I think...