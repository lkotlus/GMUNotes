### Continuing on Eigenvalues
- We're using our characteristic equation to solve systems of differential equations: $$(a-\lambda)(d-\lambda)-bc=0$$
- After that, we get our slopes with either: $$(a-\lambda_n)x+by=0$$ $$cx+(d-\lambda_n)y=0$$
- So then, we should get a slope $m_1$. Our general solution will then be: $$\begin{bmatrix}x(t)\\y(t)\end{bmatrix}=C_1e^{\lambda_1t}\begin{bmatrix}1\\m_1\end{bmatrix}+C_2e^{\lambda_2t}\begin{bmatrix}1\\m_2\end{bmatrix}$$
- Neat!

### Special Case for Systems
- Warm up:
	- Read equations with meaning.
		1. The second derivative of $x$ is equal to itself times negative one: $$\frac{d^2x}{dt^2}=-x$$
		2. $x$ added to its own second derivative is equal to zero: $$\frac{d^2x}{dt^2}+x=0$$
		3. $x$ multiplied by four and added to it's own second derivative is equal to zero: $$\frac{d^2x}{dt^2}+4x=0$$
		4. The second derivative of $x$ is itself.
	- Guess the functions:
		1. We have $x(t)=\sin(t)$ and $x(t)=\cos(t)$
		2. Same for this, $x(t)=\sin(t)$ and $x(t)=\cos(t)$
		3. A bit more complicated, $x(t)=\sin(2t)$ and $x(t)=\cos(2t)$ (double chain rule to get $2(2)=4$)
		4. Most complicated, $x(t)=e^{t}$, $x(t)=\sinh(t)$, and $x(t)=\cosh(t)$
	- Finally a use for hyperbolic sine and cosine.
- 