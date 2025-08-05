### Finishing on Imaginary Slopes
- The general process 10 times out of 10 is going to be:
	1. Find your slopes
	2. Write the general solution with imaginary components
	3. Find two linear combinations that result in linearly independent solutions without imaginary components
	4. Write a new general solution with those two new equations

### More Traditional Methods
- Finally.
- We're going to find the solutions by finding solution exponents first. Neat.
- We've got something going on with the determinant. $ad-bc=0$, we want to find eigenvalues.
- Finding equilibrium solutions for our system: $$\frac{dx}{dt}=ax+by$$ $$\frac{dy}{dt}=cx+dy$$ Is equivalent to: $$\begin{bmatrix}a & b\\c&d\end{bmatrix}\begin{bmatrix}x\\y\end{bmatrix}=\begin{bmatrix}0\\0\end{bmatrix}$$
- We want to find Eigenvalues! We want to find the exponent $\lambda$ such that if eigensolutions (straight-line solutions) exist, we get: $$\frac{dx}{dt}=\lambda x$$ $$\frac{dy}{dt}=\lambda y$$
- This is essentially the same as saying: $$\begin{bmatrix}a & b\\c&d\end{bmatrix}\begin{bmatrix}x\\y\end{bmatrix}=\lambda\begin{bmatrix}x\\y\end{bmatrix}$$
- That's the same as saying: $$\left(\begin{bmatrix}a & b\\c&d\end{bmatrix}-\begin{bmatrix}\lambda & 0\\0 & \lambda\end{bmatrix}\right)\begin{bmatrix}x\\y\end{bmatrix}=\begin{bmatrix}0\\0\end{bmatrix}$$ $$\begin{bmatrix}a-\lambda & b\\c&d-\lambda\end{bmatrix}\begin{bmatrix}x\\y\end{bmatrix}=\begin{bmatrix}0\\0\end{bmatrix}$$
- Recall that we find our eigenvalues with the characteristic equation! $\text{det}(A-\lambda I)=0$. So really, we just want to know if: $$(a-\lambda)(d-\lambda)-bc=0$$
- Very cool. We now know that the solution on each straight line is going to be something of the form: $$Ce^{\lambda t}\begin{bmatrix}n_1\\n_2\end{bmatrix}$$
- We can then go back and just find a vector on the straight line, and that's $\begin{bmatrix}n_1\\n_2\end{bmatrix}$. It's easiest to just do $\begin{bmatrix}1\\m\end{bmatrix}$. 
- So our solutions are always just in the form: $$\begin{bmatrix}x(t)\\y(t)\end{bmatrix}=C_1e^{\lambda_1t}\begin{bmatrix}1\\m_1\end{bmatrix}+C_2e^{\lambda_2t}\begin{bmatrix}1\\m_2\end{bmatrix}$$
- We find our slope by solving the following for both lambda values: $$(a-\lambda)x+by=0$$$$cx+(d-\lambda)y=0$$