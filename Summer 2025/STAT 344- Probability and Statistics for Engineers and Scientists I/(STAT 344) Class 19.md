### Hypothesis Tests on the Mean
- Suppose that we wish to test the hypotheses: $$H_0: \mu=\mu_0$$ $$H_1: \mu\ne\mu_0$$
- If variance is known, we can just use our test statistic: $$Z_0=\frac{\overline{X}-\mu_0}{\sigma/\sqrt{n}}$$
- Well, we have rejection criteria: $$z_0>z_{\alpha/2}$$ $$z_0<-z_{\alpha/2}$$
- This makes sense, it's essentially just yanked straight out of a definition from last lecture.
- We can think of our $P$-value as the value of both tails of the distribution. If the tails have more area than the center of the graph, we have a problem.
	- $z_0$ is area to the right of our upper-bound.
- Example:
	- Specifications require that mean burning rate must be $\mu=50$. Standard deviation is $\sigma=2$, significance level is $\alpha=0.05$, and our sample has $n=25$. Sample mean is $\overline{x}=51.3$.
	- So we just need to find $z_0$ and $z_{\alpha/2}=z_{0.025}$.
	- For the former, $$z_0=\frac{51.3-50}{2/\sqrt{25}}=3.25$$
	- So now we just need to go to our $z$-table for $z_{0.025}$. There, we find that $z_{0.025}=1.96$.
	- Very cool! So we can see that: $$-z_{\alpha/2}<z_0$$ $$z_{\alpha/2}<z_0$$
	- This means that we have rejection criteria number 1, so we have found that the null hypothesis is false.
	- We can also do this by checking if our $P$-value is less than $\alpha$. In this case: $$2(1-0.99942)=0.00116$$
	- This is less than $\alpha$, so this confirms that the null hypothesis is false.

### Large-Sample Test
- A test procedure for the null hypothesis were $\sigma^2$ is unknown is a very common thing in practical application.
- If $n$ is large (say, $n\ge40$) the sample standard deviation, $s$, can be substituted for $\sigma$ in the test procedures.
- So if we have a normal distribution with unknown variance, it can be converted into a large-sample test procedure.
- Exact treatment of the case where the population is normal, $\sigma^2$ is unknown, and $n$ is small involves use of the $t$ distribution: $$T_0=\frac{\overline X-\mu_0}{s/\sqrt{n}}$$
- If we're using the $t$ distribution, our rejection criteria are: $$t_0>t_{\alpha/2,n-1}$$ $$t_0<-t_{\alpha/2,n-1}$$
- Same stuff as with $z$, but with $t$.
- Sometimes the $t$ table isn't exact enough, so you need to show your $P$ value as a potential range.

### Binomial Proportion
- We can do this same stuff with our binomial proportion: $$Z_0=\frac{\overline{X}-np_0}{\sqrt{np_0(1-p_0)}}$$
- This can be done with all forms of the $Z$ test statistics and approximations.