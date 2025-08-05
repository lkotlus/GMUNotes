### Paired $t$-Test
- Null hypothesis: $$H_0: \mu_D=\Delta_0$$
- Test statistic: $$T_0=\frac{\overline{D}-\Delta_0}{S_0/\sqrt{n}}$$
- Rejection criteria and whatnot are all standard. $D$ denotes the difference. So this is average difference.
- ***<u>IF ALPHA ISN'T GIVEN, IT IS 0.05!!!!!</u>***
- Example:
	- We have two methods of doing something. Determine if there is a difference.
	- Null hypothesis: $$H_0: \mu_D=0$$
	- Alternative hypothesis: $$H_1:\mu_D\ne0$$
	- $s_d=0.1350$
	- $\overline d=0.2769$
	- $n=9$
	- $\Delta_0=0$
	- $\alpha=0.05$
	- So now we can get our test statistic: $$t_0=\frac{0.2769-0}{0.1350/3}=6.15$$
	- And now we just need to get the $P$-value. From the table, it's less than 0.001, which is very clearly less than 0.05, so we can see that we reject $H_0$.
	- We can very strongly see that there is a difference between the two.
- Intervals: $$\overline d - t_{\alpha/2,n-1}\frac{s_d}{\sqrt{n}}\le\mu_d\le\overline d + t_{\alpha/2,n-1}\frac{s_d}{\sqrt{n}}$$
- ***EXAMPLE 10.12 ON THE FINAL*** (potentially)

### Large-Sample Tests on the Difference Population Proportions
- If we're testing: $$H_0: p_1=p_2$$
We will use: $$Z=\frac{\widehat P_1 - \widehat P_2 - \Delta_0}{\sqrt{\frac{p_1(1-p_1)}{n_1} + \frac{p_2(1-p_2)}{n_2}}}$$ $$Z_0=\frac{\widehat P_1 - \widehat P_2 - \Delta_0}{\sqrt{\widehat P(1-\widehat P)\left(\frac{1}{n_1} + \frac{1}{n_2}\right)}}$$
- Classic criteria here, nothing out of the ordinary.
- Example, it seems unnecessary.
- Confidence interval is the same old thing: $$\widehat p_1-\widehat p_2-z_{\alpha/2}\sqrt{\frac{\widehat p_1(1-\widehat p_1)}{n_1} + \frac{\widehat p_2(1-\widehat p_2)}{n_2}}\le p_1-p_2\le...$$
- There's an example for this one as well.

### Summary table at the end of the slides.