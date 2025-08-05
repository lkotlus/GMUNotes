### Warm-up
- A tank initially contains 15 G of saltwater containing 6 lbs of salt. Saltwater containing 1 lb of salt/G is pumped into the top of the tank at a rate of 2 G/min, while a well-mixed solution leaves the bottom at a rate of 1 G/min.
- Should the rate of change equation for the salt in this situation depend just on the amount of salt $S$ in the tank, the time $t$, or both? Explain?
	- It can't just be salt, so it's either $t$ or $S$ and $t$.
	- This entire question is wrinkling my brain. I just want to model an equation, but I don't know how. I hate this.
	- We depend on the amount of salt in the tank to know how much salt is leaving the tank, so we also need $S$.
- $S$ and $t$.
- Today we get to use the reverse product rule (integrating factor method)!

### Integrating Factor
- The general rule of thumb for setting up a rate of change equation is $\text{RoC}=\text{rate in} - \text{rate out}$. So for this, we can just do some dimensional analysis.
- So we need everything in lbs/min, so we need that to be the units for everything we get. So for now, $\frac{dS}{dt}=2-\text{rate out}$. Easy.
- We have the flow coming out as 1 g/min. We can multiply this by the concentration equation, which is going to be salt divided by the current amount of water. 
- That's $\frac{S}{2t+15-t}=\frac{S}{2t+15}$.
- So we have something in the form $\frac{dy}{dt}+g(t)\cdot y = r(t)$. This is called a linear DE. There's lots of ways to solve them.
- $u=e^{\int g(t)\ dt}$, because we can see that $\frac{du}{dt}=u\cdot g(t)$, which gives us $\frac{1}{u}\ du=g(t)\ dt$, which gives that $\int\frac{1}{u}\ du=\int g(t)\ dt$. From that, $ln|u|+C=\int g(t)\ dt$. We can choose $C=0$ and positive $u$, because it doesn't matter so long as our function works. $u=e^{\int g(t)\ dt}$.