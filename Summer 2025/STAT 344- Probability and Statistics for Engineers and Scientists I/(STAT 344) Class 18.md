### Tests of Hypotheses for a Single Sample
- Outline and whatnot
- Learning objectives
	1. Structure engineering decision-making problems as hypothesis tests
	2. Test hypotheses on the mean of a normal distribution using a $Z$-test or a $t$-test
	3. Test hypotheses on a population proportion
	4. Use the $P$-value approach for making decisions in hypothesis tests
	5. Computer power and Type II error probability and make sample size selection decision for tests on means and proportions
	6. Explain and use the relationship between confidence intervals and hypothesis tests

### Introduction
- In the previous chapter, we did confidence intervals
- Many problems in engineering require that we decide which of two completing claims is true
- The statements are called hypotheses, and the procedure here is hypothesis testing.
	- This is highly useful
- For example, suppose that an engineer is designing an air crew escape system that consists of an ejection seat and a rocket motor that powers the seat
	- The rocket motor should have a mean burning rate of 50 cm/sec
	- If it's too low, the ejection seat may not function properly
	- If it's too high, we introduce instability
	- So we need to ask whether or not the mean burning rate is equal to 50 cm/sec
	- This type of question can be answered using hypothesis testing

### Hypothesis Testing
- Statistical hypothesis
	- A statistical hypothesis is a statement about the parameters of one or more populations
- Two-sided alternative hypothesis
	- Let $H_0$: $\mu=50$ cm/sec, and $H_1$: $\mu\ne 50$ cm/sec
		- The first statement is the null hypothesis
		- The latter is the alternate hypothesis
- One-sided alternative hypothesis
	- Left side
		- $H_0$: $\mu=50$ cm/sec
		- $H_1$: $\mu<50$ cm/sec
	- Right side
		- $H_0$: $\mu=50$ cm/sec
		- $H_1$: $\mu>50$ cm/sec
- In our text and in this course, we always state the null hypothesis as an equality claim.
- When the alternative hypothesis is stated with the $<$ sign, the implicit claim in the null hypothesis can be taken as $\ge$.
	- And vice-versa
- It's important to remember that hypotheses are always statements about the population or distribution under study, not statements about the sample.
- Example
	- Continuing with the earlier example, let's do:
		- Let $H_0$: $\mu=50$ cm/sec, and $H_1$: $\mu\ne 50$ cm/sec
		- $\sigma=2.5$
		- $n=10$
	- So if we have $\overline{x}\approx\mu$, that supports the hypothesis.
	- Let's define that as $48.5\le\overline{x}\le51.5$.
		- We call this the acceptance region
	- If we have $\overline{x}<48.5\lor \overline{x}>51.5$, then that's our rejection region. The values that lie in the rejection region constitute the critical region.
	- The boundaries between the critical regions and the acceptance region are called the critical values. For us, that's 48.5 and 51.5.
	- It's customer to state conclusions relative to the null hypothesis. Therefore, we reject $H_0$ in favor of $H_1$ if the test statistic falls in the critical region and fails to reject $H_0$ otherwise.
- Decisions in hypothesis testing:
	- Fail to reject $H_0$
		- $H_0$ is true: no error
		- $H_0$ is false: Type II error
	- Reject $H_0$:
		- $H_0$ is true: Type I
		- $H_0$ is false: no error
	- $c_1$ and $c_2$ are the lower and upper critical values respectively.
	- Probability of Type I Error: $$\alpha=P(\overline{X}<c_1)+P(\overline{X}>c_2)$$
	- Probability of a Type II Error: $$\beta=P(c_1<\overline{X}<c_2)$$
	- I think we're gonna use confidence intervals.
	- Sometimes the Type I error probability is called the significance level, or the $\alpha$-error, or the size of the test.
- Example:
	- With our current example: $$\alpha=P(\overline{X}<48.5)+P(\overline{X}>51.5)\ \ \land\ \ \mu=50$$
	- We need to get our $z$-values, so first we need our standard error: $$\frac{\sigma}{\sqrt{n}}=\frac{2.5}{\sqrt{10}}=0.79$$
	- So from this, we just do: $$\frac{\overline{X}-\mu}{\text{SE}}$$ $$\frac{48.5-50}{0.79}=-1.90, \ \ \ \frac{51.5-50}{0.79}=1.90$$
	- So therefore: $$\alpha=P(z<-1.9)+P(z>1.9)=0.0287+0.0287=0.0574$$
	- So we have a 5.74% chance of a Type I error.
	- If we want to lower this, we can either increase our acceptance region or increase our sample size.
- Example:
	- Now let's find Type II error, assuming that $\mu=52$.
	- So we want to know: $$\beta=P(48.5<\overline{X}<51.5)=P(\overline{X}<51.5)-P(\overline{X}<48.5)$$
	- Let's get $z$-values: $$\frac{48.5-52}{0.79}=-4.43$$ $$\frac{51.5-52}{0.79}=-0.63$$
	- And so from there, $$\beta=P(48.5<\overline{X}<51.5)=0.2643-0.0000=0.2643$$
	- So there's a 26.43% chance that we fail to reject the false null hypothesis! That's huge!
- Important things:
	1. The size of the critical region, and consequently the probability of a Type I error ($\alpha$), can always be reduced by appropriate selection of the critical values.
	2. Type I and Type II errors are related. The values of $\alpha$ and $\beta$ are inversely correlated (assuming $n$ is constant).
	3. An increase in the sample size reduces $\beta$, provided that $\alpha$ is held constant.
	 4. When the null hypothesis is false, $\beta$ increases as the true value of the parameter approaches the value hypothesized in the null hypothesis. The value of $\beta$ decreases as the difference between the true mean and the hypothesized value increases.

### Power of a Statistical Test
- Definition
	- The power of a statistical test is the probability of rejecting $H_0$ when $H_1$ is true.
	- In layman's terms, the probability of correctly rejecting a false null hypothesis.
- This is equal to $1-\beta$.
- So with our 26.43% chance of Type II from above, we know that there's a 73.57% chance that we correctly detect that the null hypothesis is false.

### One and Two-Sided Hypotheses
- In formulating one-sided alternative hypotheses, we should remember that rejecting $H_0$ is always a strong conclusion. 
- Consequently, we should put the statement about which it is important to make a strong conclusion in the alternative hypothesis. 
- In real-world problems, this will often depend on our point of view and experience with the situation.

### $P$-Value
- Definition
	- The smallest level of significance that would lead to rejection of $H_0$ with the given data.
- This is the observed significance level.
- The probability that the test statistic will take on a value that is at least as extreme as the observed value of the statistic when $H_0$ is true.
- $P$-value less than $\alpha$:
	- Reject
- $P$-value greater than or equal to $\alpha$:
	- Fail to reject
- Essentially, take the difference between $\overline{X}$ and $\mu$, and use that to create your acceptance region. Then find $1-P(\text{LB}<\overline{X}<\text{UB})$.
- Example:
	- With $\mu=50$, $n=16$, $\sigma=2.5$, and $\overline{x}=51.3$.
	- The upper bound is just 51.3
	- The difference between the sample mean and population mean is 1.3, so our lower bound is: $\mu-1.3=50-1.3=48.7$.
	- So we just need to find: $$1-P(48.7<\overline{X}<51.3)=0.038$$

### Connection Between Hypothesis Tests and Confidence Intervals
- A close relationship exists between the test of a hypothesis for $\theta$ and the confidence interval for $\theta$.
- If $[l,u]$ is a $100(1-\alpha)\%$ confidence interval for the parameter $\theta$, then the test of size $\alpha$ of the hypothesis: $$H_0: \theta=\theta_0$$ $$H_1:\theta\ne\theta_0$$ will lead to rejection of $H_0$ iff $\theta_0$ is not in the $100(1-\alpha)\%$ confidence interval.
- Essentially, if our hypothesized value is not in the confidence interval then we will reject it.

### General Procedure
1. Find the parameter of interest
2. State $H_0$
3. State $H_1$
4. Find a test statistic
5. Reject $H_0$ if possible
6. Compute any necessary sample quantities
7. Draw conclusions

