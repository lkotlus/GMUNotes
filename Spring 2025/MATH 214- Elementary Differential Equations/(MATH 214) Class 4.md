### Starting where we left off
- So we have a slope field for $\frac{dP}{dt}=0.3P(1-\frac{P}{10})$. We want to do our little "tip-to-tail" method on it.
- So we started off at $t=0$ with the initial condition of 8 fish in the lake, and we saw how that works.
- Now, what if we start off at $P=10$? What if it's slightly less or more than 10?
	- So if we start at 10 we flatline.
	- If we start at either slightly less or more we just go to 10 and flatline.
- What about for $P=0$?
	- If we are $= 0$, then we flatline at 0.
	- If we are $\gt 0$, then we go to 10 and flatline. 
	- If we are $\lt 0$, then we go to $-\infty$.
- This makes sense, although it would seem as if different equilibrium solutions have different behaviors. Some have solutions drawn towards them ($P=10$), others propel them away ($P=0$).
- Some terms that come to mind are converging/diverging, stable/unstable, etc.
- $P=10$ is stable. $P=0$ is unstable.
- With this slope field, how are we thinking about rate of change for our approximation method?
	- So we think of rate of change as always changing, but we treat them as constant over certain intervals.
	- Follow up 1: why is the graph an approximation?
		- Because the rate of change is always changing, yet we treat it as constant over an interval. The more intervals, the more truthful we are to the change experienced, and therefore the more accurate of a result we get.
	- Follow up 2: what different quantities are held constant to create the graph?
		- We just hold $\frac{dP}{dt}$ constant over certain intervals of $t$.
		- Size of intervals is also constant.

|$t$|$P$|$\frac{dP}{dt}$|
|-|-|-|
|0|10|5|
|0.5|12.5|4.69|
|1|14.85|3.82|
|1.5|16.67|2.78|

### Generalizing This
- So we just want something like: $$y_n=\left(\frac{dy}{dt}|_{y_{n-1},\ \ \Delta t(n-1)}\right)(\Delta t)+y_{n-1}$$
- <u>**Euler's Method!**</u>