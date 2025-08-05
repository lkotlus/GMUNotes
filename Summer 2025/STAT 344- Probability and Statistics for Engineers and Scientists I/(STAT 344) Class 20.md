### Statistical Inference for Two Samples
- Outline and whatnot
- Learning objectives
	1. Structure comparative experiments involving two samples as hypothesis tests
	2. Test hypotheses and construct confidence intervals on the difference in means of two normal distributions
	3. Test hypotheses and construct confidence intervals on the difference in two population proportions
	4. Use the $P$-value approach for making decisions in hypothesis tests
	5. Explain and use the relationship between confidence intervals and hypothesis tests

### Inference on the Difference in Means of Two Normal Distributions, Variance Known
- Assumptions
	1. Let $X_{11},X_{12},X_{1n_1}$ be a random sample from population 1
	2. Let $X_{21},X_{13},X_{2n_1}$ be a random sample from population 2
	3. The two populations $X_1$ and $X_2$ are independent
	4. Both $X_1$ and $X_2$ are normal.
- From this, $$E(\overline{X}_1-\overline{X}_2)=E(\overline{X}_1)-E(\overline{X}_2)=\mu_1-\mu_2$$ $$V(\overline{X}_1-\overline{X}_2)=V(\overline{X}_1)-V(\overline{X}_2)=\frac{\sigma_1^2}{n_1}+\frac{\sigma_2^2}{n_2}$$
- The quantity: $$Z=\frac{\overline{X}_1-\overline{X}_2-(\mu_1-\mu_2)}{\sqrt{\frac{\sigma_1^2}{n_1}+\frac{\sigma_2^2}{n_2}}}$$ has an $N(0,1)$ (standard normal) distribution
- Recall that we still require the Central Limit Theorem to be fulfilled.
- Some things:
	- Null hypothesis: $$H_0:\mu_1-\mu_2=\Delta_0$$
	- Test statistic: $$Z_0=\frac{\overline{X}_1-\overline{X}_2-\Delta_0}{\sqrt{\frac{\sigma_1^2}{n_1}+\frac{\sigma^2_2}{n_2}}}$$
	- Alternative Hypotheses:
		- $H_1: \mu_1-\mu_2\ne \Delta_0$
			- $P$-value: probability above $|z_0|$ and probability below $-|z_0|$, $P=2[1-\Phi(|z_0|)]$
			- Rejection criteria: $z_0>z_{\alpha/2}$ or $z_0<-z_{\alpha/2}$
		- $H_1: \mu_1-\mu_2>\Delta_0$
			- $P$-value: probability above $z_0$, $P=1-\Phi(z_0)$
			- Rejection criteria: $z_0>z_{\alpha/2}$
		- $H_1: \mu_1-\mu_2<\Delta_0$
			- $P$-value: probability below $z_0$, $P=\Phi(z_0)$
			- Rejection criteria: $z_0<-z_{\alpha/2}$
- A lot of the same stuff there.
- Example:
	- $\sigma_1^2=\sigma_2^2=64$
	- $n_1=n_2=10$
	- $\overline{x}_1=121$
	- $\overline{x}_2=112$
	- $\alpha=0.05$
	- $\Delta_0=0$
	- $H_0:\mu_1-\mu_2=0$
	- $H_1:\mu_1-\mu_2>0$
	- From this, we can go ahead and look at our test statistic: $$z_0=\frac{121-112-0}{\sqrt{\frac{64}{10}+\frac{64}{10}}}$$ $$z_0=\frac{9}{\sqrt{\frac{128}{10}}}$$ $$z_0\approx2.515576475$$
	- We can reject the null hypothesis if the $P$-value is less than $\alpha$.
	- So let's just find $1-\Phi(z_0)$: $$P=1-\Phi(z_0)=0.00587$$
	- From this, our $P$-value is far less than $\alpha$, and so we reject $H_0$. We can conclude that the new ingredient significantly reduces the drying time.
- Confidence interval shenanigans: $$\overline x_1-\overline x_2-z_{\alpha/2}\sqrt{\frac{\sigma_1^2}{n_1}+\frac{\sigma_2^2}{n_2}}\le\mu_1-\mu_2\le\overline x_1-\overline x_2+z_{\alpha/2}\sqrt{\frac{\sigma_1^2}{n_1}+\frac{\sigma_2^2}{n_2}}$$
	- We just use that like we would for any confidence interval. Same precedence with one-sided tests as well, just use $z_\alpha$ rather than $z_{\alpha/2}$ and go with the upper or lower bound.
- Choice of Sample Size:
	- Sample size for a confidence interval on the difference in means with variance known can be found by: $$n=\left(\frac{z_{\alpha/2}}{E}\right)^2)(\sigma_1^2+\sigma_2^2)$$
	- Round up if $n$ is not an integer. This ensures that the level of confidence does not drop below $100(1-\alpha)\%$
- We will go into some unknown variance things in the next lecture.