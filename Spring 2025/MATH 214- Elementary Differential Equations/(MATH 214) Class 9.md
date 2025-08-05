### Warm-up
- The following two DEs predict the height of a helicopter as it nears the ground: $$\frac{dh}{dt}=-h$$ $$\frac{dh}{dt}=-h^{\frac{1}{3}}$$
	- As $h\rightarrow 0$, what can you say about $\frac{dh}{dt}$ and what does that imply about whether the model predicts that the helicopter lands?
		- Change in height decreases to zero in both instances, so the helicopter doesn't necessarily *land*, but it does stop moving vertically.
	- Sketch your best guess for a height versus time solution graph for each DE.
		- Graphs.

### Uniqueness and Existence
- Do we have solutions? Are the solutions special?
- Recall reverse product and separation of variables.
- How do we know when we *can* solve a differential equation?
- Working from the warm up, what do the DEs say about the solution if the helicopter is already on the ground?
	- Both of them just show that we should have a flat line at $h=0$.
	- **<u>Equilibrium solution !!!</u>**
- Interpret the initial condition $h(0)=0$ and explain why $h(t)=0$ should be a solution to each differential equation under this initial condition.
	- If $h$ is zero, then the helicopter is on the ground. The slope at $h=0$ is $0$, so we know that it's just landed and staying still.
	- Furthermore, $\frac{d}{dt}[0]=0$, so if $h(t)=0$, then $\frac{dh}{dt}=0$ as well, which fits our DE.
- Sketch solution curves for each DE. For each DE, graph 1 solution with IC $h(0)=0$ and another with $h(0)=0.2$.
	- DE 1 (blue), DE 2 (red), both with $h(0)=0$ (green).
	- ![[Pasted image 20250218124318.png]]
- Solve the IVPs for $\frac{dh}{dt}=-h$:
	- $h(0)=2$
		- $h(t)=2e^{-t}$
	- $h(0)=0$
		- $h(t)=0$
- Solve the IVPs for $\frac{dh}{dt}=-h^{\frac{1}{3}}$:
	- $h(0)=2$
	- Piecewise function:
	$$
	h(t)=\begin{cases}
	\left(-\frac23t+2^\frac23\right)^\frac32 & h>0\\
	0 & h=0
	\end{cases}
	$$
	- $h(0)=0$
		- $h(t)=0$