### Finishing Up Laplace Transforms
- Partial fractions!
- Recall that: $$\mathscr{L}\left\{e^{at}\right\}=\frac{1}{s-a}$$
- By Euler's Formula: $$\mathscr{L}\left\{e^{i\beta t}\right\}=\mathscr{L}\left\{\cos(\beta t)\right\}+i\mathscr{L}\left\{\sin(\beta t)\right\}$$
- What's the Laplace transform of our trig functions? $$\mathscr{L}\left\{\cos(\beta t)\right\}=\frac{s}{s^2+\beta^2}$$$$\mathscr{L}\left\{\sin(\beta t)\right\}=\frac{\beta}{s^2+\beta^2}$$
- We can get those by observing coefficients. $$\frac{1}{s-i\beta}=\mathscr{L}\left\{\cos(\beta t)\right\}+i\mathscr{L}\left\{\sin(\beta t)\right\}$$ $$\frac{s+i\beta}{s^2+\beta^2}=\mathscr{L}\left\{\cos(\beta t)\right\}+i\mathscr{L}\left\{\sin(\beta t)\right\}$$ $$\frac{s}{s^2+b^2}+i\frac{\beta}{s^2+\beta^2}=\mathscr{L}\left\{\cos(\beta t)\right\}+i\mathscr{L}\left\{\sin(\beta t)\right\}$$
- Neat.
- There's some special functions called the Dirac $\delta$-function and the Heaviside function. Their Laplace transforms are: $$\mathscr{L}\left\{H_c(t)f(t-c)\right\}=e^{-sc}\mathscr{L}\left\{f(t)\right\}$$ $$\mathscr{L}\left\{\delta(t-a)\right\}=\mathscr{L}\left\{\delta_a(t)\right\}=e^{-sa}$$
- 