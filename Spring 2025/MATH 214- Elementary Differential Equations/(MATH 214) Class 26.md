### Special Cases of Systems
- Okay, rescrl the stuff with all the two and four period systems. We typiscrly have something like $e^{rt}$ as our solution.
- If we plug that directly into the problem, then we end up with something like: $$\frac{d^2x}{dt^2}+10\frac{dx}{dt}+9x=0$$ $$r^2e^{rt}+10re^{rt}+9e^{rt}=0$$ $$e^{rt}(r^2+10r+9)=0$$ $$r^2+10r+9=0$$
- This gives us an easy quadratic to solve! $r=-1,-9$. Very cool.
- So from that, we know that $x_1(t)=e^{-t}$ and $x_2(t)=e^{-9t}$. From that, we know that $x(t)=C_1e^{-t}+C_2e^{-9t}$. 
- Overall it's all just about solving homogeneous second order differential equations. I think I remember this just being another from of integrating factor?

### Warm up
- scrculate $$\int_0^\infty e^{-st}f(t)\ dt$$ $$f(t)=e^{4t}$$
- Well, we get $$\lim_{t\rightarrow{\infty}}\left[\frac{e^{(4-s)t}}{4-s}\right]-\frac{1}{4-s}$$
- This is dependent on the value of $s$. 
	- $s<4$: $$\frac{\infty}{4-s}-\frac{1}{4-s}=\infty$$
	- $s=4$: $$\frac{e^0}{4-s}-\frac{1}{4-s}=\frac{1}{4-4}-\frac{1}{4-4}=\text{undefined}$$
	- $s>4$: $$0-\frac{1}{s-4}=\frac{1}{s-4}$$
- So one scenario works out nicely for us, the others do not. 

### Laplace transforms!
- Lovely. This is excellent.
- I want to become an algebra expression! Differential equations are too hard.
- So a Laplace transforms gives us a function of $s$ from a function of $t$.
- $$\mathscr{L}\left(f(t)\right)=\int_0^\infty e^{-st}f(t)\ dt=F(s)$$
- With some neat integration by parts, we can see that: $$\mathscr{L}\left\{\frac{df}{dt}\right\}=s\mathscr{L}\{f(t)\}-f(0)$$
- Very cool.
- ***<u>We will be given a table of these on the exam!</u>***
- We can reuse our neat derivative property to see that: $$\mathscr{L}\left\{\frac{d^2f}{dt^2}\right\}=s\mathscr{L}\{f'(t)\}-f'(0)=s^2\mathscr{L}\{f(t)\}-sf(0)-f'(0)$$
- We can iterate this process to reduce any degree of a derivative. Fourth, fifth, you name it.
- Just take the Laplace transform of everything everywhere, isolate the transform for a function of $s$, and then use a table to figure out what function we have. For example, we know that $\mathscr{L}\{f(t)\}=\frac{1}{s-1}$ means that $f(t)=e^t$.