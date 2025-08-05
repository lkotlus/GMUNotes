### Warm-up
- Is the DE $\frac{dh}{dt}=-h+1$ separable? Why or why not?
- It is, because we can divide both sides by $-h+1$ and multiply both sides by $dt$ to get $\frac{1}{1-h}\ dh=dt$.
- $h=ke^{-t}-1$

### Analytic approach
- We want to get exact answers to things!
- Today we have particular solutions. Rather than an infinite set of functions, let's take an initial value to get the perfect solution.
- For example:
	- Solve the IVP: $\frac{dy}{dt}=\frac{t}{y}$, $y(2)=-1$
	- $y=-\sqrt{t^2-3}$.
	- Valid for $t\ge\sqrt{3}$ (choosing positive because our initial value is positive)
- If your initial value still gives two possible functions, we don't have a unique solution.
- We can shift any autonomous differential equation by a constant to get the particular solution for a different initial value.