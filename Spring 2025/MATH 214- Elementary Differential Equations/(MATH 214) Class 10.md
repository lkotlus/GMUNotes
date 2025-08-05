### Uniqueness and Existence
- Recall that sometimes we can have piecewise solutions to things:
$$
h(t)=\begin{cases}
\left(\frac23\left(-t+\frac{3}{\sqrt[3]{2}}\right)\right)^\frac32 & t\le\frac{3}{\sqrt[3]{2}}\\
0 & t>\frac{3}{\sqrt[3]{2}}
\end{cases}
$$
- Notice that we can generalize:
$$
h(t)=\begin{cases}
\left(\frac23\left(-t+C\right)\right)^\frac32 & t\le C\\
0 & t>C
\end{cases}
$$
- The issue that arises here is that $h(0)=0$ results in two solution functions: 
$$
h(t)=\begin{cases}
\left(\frac23\left(-t\right)\right)^\frac32 & t\le 0\\
0 & t>0
\end{cases}
$$
$$h(t)=0$$
- We lose the predictive power of a DE when solutions touch/cross.
- **<u>Definitions</u>**:
	- Unique/uniqueness:
		- Refers to whether or not two solution functions ever touch/cross each other. Solutions are unique if IVP solutions do not cross.
		- We don't always have to analytically solve to determine if IVP solutions will or will not be unique.
		- The Uniqueness Theorem determines what values we are unique for.
- Formal Uniqueness Theorem:
	- Let $f(x,y)$ be a real valued function that is continuous on the rectangle $R=\left\{(x,y):|x-x_o|\le a,|y-y_o|\le b\right\}$
	- Informally, we want to know if solutions to a DE $\frac{dy}{dt}=f(y,t)$ don't touch in some rectangular region. If $\frac{\partial}{\partial y}\left[\frac{dy}{dt}\right]$ is continuous on the region, we are unique.
- Existence:
	- How do we even know that we have a solution to a DE?
	- If we are continuous in the $y$-$t$-region containing the IC, then a solution to the IVP exists.