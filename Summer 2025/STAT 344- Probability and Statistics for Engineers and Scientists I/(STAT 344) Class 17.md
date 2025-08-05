### Statistics and Intervals for a Single Sample
- Chapter outline and whatnot.
- Objectives
	1. Construct confidence intervals on teh mean of a normal distribution, using normal distribution or $t$ distribution methods
	2. Construct confidence intervals on a population proportion
	3. Use a general method for constructing an approximate confidence interval on a parameter

### Introduction
- A confidence interval for a parameter is an interval computed from sample data by a method that will capture the parameter for a specified proportion of all samples.
- Confidence intervals supplement a statistic with an indication of the statistic's variability. General form is: $$\text{sample}\pm\text{margin}$$
- A confidence interval is an interval, computed from a sample, that has a predetermined chance of capturing the value of the population parameter.
- Remember, parameters are fixed values, but sample statistics vary from sample to sample.
- The method used to construct a confidence interval should capture the parameter for a predetermined proportion of all possible samples
- Some samples will give intervals that contain the parameter and some will give intervals that miss the target
- Confidence intervals provide us with
	- A range of plausible values for a population parameter
	- A confidence level, which expresses our level of confidence that the interval contains the population parameter
- A confidence interval always specifies a confidence level, usually 90%, 95%, or 99%, which is a measure of the reliability of the procedure.
- By reliability, we mean if we repeated the experiment over and over again, the percentage of all the samples would produce a confidence interval that contains or captures the true unknown population parameter.

### Confidence Interval and Properties
- A confidence interval estimate for $\mu$ is an interval of the form $l\le\mu\le u$, where the end-end points $l$ and $u$ are computed from the sample data.
- Because different samples will produce different values of $l$ and $u$, these end-points are values of random variables $L$ and $U$, respectively
- Suppose that we can determine values of $L$ and $U$ such that the following probability statement is true: $$P(L\le \mu\le U)=1-\alpha$$
- A confidence interval estimate for $\mu$ is an interval of the above form, where the end-points $L$ and $U$ are computed from the sample data and $0\le\alpha\le1$. 
	- There is a probability of $1-\alpha$ of selecting a sample for which the CI will contain the true value of $\mu$.
	- The endpoints or bounds $L$ and $U$ are called lower and upper-confidence limits, and $1-\alpha$ is the confidence coefficient
- Once we have selected the sample such that $X_1=x_1, X_2=x_2, ...$, and computed $l$ and $u$, the resulting confidence interval for $\mu$ is: $$l\le\mu\le u$$
- In our problem situation, because $Z=\frac{\overline{X}-\mu}{\sigma\cdot n^{-\frac12}}$. has a standard normal distribution, we may write: $$P\left\{-z_{\alpha/2}\le\frac{\overline{X}-\mu}{\sigma/\sqrt{n}}\le z_{\alpha/2}\right\}=1-\alpha$$

### Confidence Interval on the Mean and Variance Known
- If $\overline x$ is the sample mean of a random sample of size $n$ from a normal population with known variance $\sigma^2$, a $1-\alpha$ confidence interval on $\mu$ is given by $$\overline{x}-z_{\alpha/2}\frac{\sigma}{\sqrt{n}}\le\mu\le\overline{x}+z_{\alpha/2}\frac{\sigma}{\sqrt{n}}$$ where $z_{\alpha/2}$ is the upper $\alpha/2$ probability point of the standard normal distribution.
- Example:
	- Ten measurements of impact energy ($\text{J}$) on specimens of A238 steel cut at 60 degrees Celsius are as follows: (numbers). The impact energy is normally distributed with $\sigma=1\text{ J}$. Find a 95% CI for $\mu$, the mean impact energy.
	- We have $\sigma=1\text{ J}$, which tells us that $\sigma^2=1\text{ J}^2$.
	- So our first step is finding $\overline{x}$. This is easy enough, we just sum up the values and divide by $n=10$. This comes out to $\overline{x}=64.46$
	- Next, $1-\alpha=0.95$, so $\alpha=0.05$. We need $z_{\alpha/2}=z_{0.025}$, which denotes the $z$ such that $P(Z>z)=0.025$. So we're looking for $P(Z>z_{0.025})=0.025$. We can only look at cumulative values, so this is equivalent to $P(Z<z_{0.025})=0.975$, which tells us that $z_{0.025}=1.96$.
	- From this, $64.45-\frac{1.96}{\sqrt{10}}\le\mu\le 64.46+\frac{1.96}{\sqrt{10}}$, which gives: $$63.84\le\mu\le 65.08$$
	- So we know that a range of highly plausible values for mean impact energy of A238 steel at 60 degrees Celsius is $$63.84\text{ J}\le\mu\le 65.08\text{ J}$$

### Choice of Sample Size
- Sample size for specified error on the mean and variance known:
	- If $\overline x$ is used as an estimate of $\mu$, we can be $100(1-\alpha)$ percent confident that the error $|\overline x - \mu|$ will not exceed a specified amount $E$ when the sample size is: $$n=\left(\frac{z_{\alpha/2}\sigma}{E}\right)^2$$
	- Essentially, we can choose a probable maximum difference between sample and population mean based on sample size
- Example
	- Consider the CVN test in the previous example. Determine how many specimens must be tested to ensure that 95% CI on $\mu$ for A238 steel cut at 60 degrees Celsius has a length of at most $1.0\text{ J}$.
	- We are given the bound on error in the estimation is $E=\frac{\text{CI}}{2}$, so $E=0.5$.
	- So we want $0.95=1-\alpha$, so $\alpha=0.05$.
	- From this, $$n=\left(\frac{(1.96)(1.0)}{0.5}\right)^2=\lceil15.21\rceil=16$$

### One-Sided Confidence Bounds
- A $100(1-\alpha)$ percent upper-confidence bound for $\mu$ is: $$\mu\le \overline{x}+\frac{z_\alpha\sigma}{\sqrt{n}}$$
- A $100(1-\alpha)$ percent lower-confidence bound for $\mu$ is: $$\mu\ge \overline{x}-\frac{z_\alpha\sigma}{\sqrt{n}}$$
- Example
	- Same testing data, used to construct a lower-confidence bound for 95% confidence interval of the mean impact energy.
	- So we have: $$\mu\ge 64.46-\frac{1.64\cdot 1}{\sqrt{10}}$$ $$\mu\ge 63.94$$
	- So we are 95% sure that the population mean will be greater than or equal to $63.94\text{ J}$.

### Large-Sample Confidence Interval on the Mean
- When $n$ is large, the quantity $$\frac{\overline X - \mu}{S/\sqrt{n}}$$ has an approximate standard normal distribution. Consequently, $$\overline{x}-z_{\alpha/2}\frac{s}{\sqrt{n}}\le\mu\le\overline{x}+z_{\alpha/2}\frac{s}{\sqrt{n}}$$ is a large-sample confidence interval for $\mu$ with confidence level of approximately $100(1-\alpha)$ percent.
- Example
	- A sample of fish was selected from 53 Florida lakes, and mercury concentration int he muscle tissue was measured (ppm). The mercury concentration values were: (lots of numbers).
	- Find an approximate 95% CI on $\mu$.
	- So $\alpha=0.05$. We are given that $n=53$ and can easily calculate:
		- $\overline{x}=0.5250$
		- $\widetilde{x}=0.4900$
		- $s=0.3486$
		- Minimum: 0.0400
		- Maximum: 1.3300
		- First Quantile: 0.2300
		- Third Quantile: 0.7900
	- Cool. So from this, we just know that $$\overline{x}-z_{\alpha/2}\frac{s}{\sqrt{n}}\le\mu\le\overline{x}+z_{\alpha/2}\frac{s}{\sqrt{n}}$$ $$0.5250-\frac{(1.96)(0.3486)}{\sqrt{53}}\le\mu\le0.5250+\frac{(1.96)(0.3486)}{\sqrt{53}}$$ $$0.431\le\mu\le0.619$$
	- So we can be confident that our mean has a 95% chance of being in that range. This range is large, but that's because we have such high variability (0.59, which is larger than the mean).

### Large-Sample Approximate Confidence Interval
- Suppose that $\theta$ is a parameter of a probability distribution, and let $\widehat \theta$ be an estimator of $\theta$. Then a large-sample approximate CI for $\theta$ is given by: $$\widehat\theta - z_{\alpha/2}\sigma_{\widehat\Theta}\le\theta\le\widehat\theta + z_{\alpha/2}\sigma_{\widehat\Theta}$$
- This is just a generalized version of what we've been doing.

### Student's $t$-Distribution
- Used when $\sigma$ is unknown.
- "Student" was the pen name of William Sealy Goesset, who introduced the $t$-statistic and $t$-test in 1908, while working for the Guinness brewery in Dublin.
- Let $X_1, ..., X_n$ be a random sample from a normal distribution with unknown mean $\mu$ and unknown variance $\sigma^2$. The random variable: $$T=\frac{\overline{X}-\mu}{S/\sqrt{n}}$$ has a $t$ distribution with $n-1$ degrees of freedom.
- If $\overline{x}$ and $s$ are the mean and standard deviation of a random sample from a normal distribution with unknown variance, a $1-\alpha$ confidence interval on $\mu$ is given by: $$\overline{x}-t_{a/2,n-1}\frac{s}{\sqrt{n}}\le\mu\le\overline{x}+t_{a/2,n-1}\frac{s}{\sqrt{n}}$$ where $t_{\alpha/2,n-1}$ is the upper $\frac{100\alpha}{2}$ percentage point of the $t$ distribution with $n-1$ degrees of freedom.
- We just use a $T$ table rather than a $Z$ table, and we need to have both probability and degrees of freedom.
- Example:
	- The load at specimen failure is as follows: (numbers, in megapascals)
	- Construct a 95% CI on $\mu$.
	- So we know that $\alpha=0.05$, $n=22$, $\overline{x}=13.71$, and $s=3.55$.
	- So We need to find $t_{0.025, 21}$. This is fairly easy with the table, $t=2.080$.
	- Now that all the variables are present, $$13.71-\frac{(2.080)(3.55)}{\sqrt{22}}\le\mu\le13.71+\frac{(2.080)(3.55)}{\sqrt{22}}$$ $$12.14\le\mu\le 15.28$$

### Large-Sample Confidence Interval Population Proportion
- Normal Approximation for a Binomial Proportion
	- If $n$ is large, the distribution of: $$Z=\frac{\overline X-np}{\sqrt{np(1-p)}}=\frac{\widehat P-p}{\sqrt{\frac{ p(1- p)}{n}}}$$ is approximately standard normal.
	- From this, we know that $$P\left(\widehat p-z_{\alpha/2}\sqrt{\frac{ p(1- p)}{n}}\le p\le\widehat p+z_{\alpha/2}\sqrt{\frac{ p(1- p)}{n}}\right)\approx 1-\alpha$$
- Example:
	- In a random sample of 85 car engine crankshaft bearings, 10 have a surface finish that is rougher than the specifications allow. Construct a 95% two-sided confidence interval for $p$.
	- Well, $n=85$ and we have $10$ failures, so $p\approx 0.12$.
	- $z_{0.025}=1.96$, so $$0.12-1.96\sqrt{\frac{0.12(0.88)}{85}}\le p\le 0.12+1.96\sqrt{\frac{0.12(0.88)}{85}}$$ $$0.051\le p\le 0.189$$

### Choice of Sample Size
- Sample Size for a Specified Error on a Binomial Proportion: $$n=\left(\frac{z_{\alpha/2}}{E}\right)^2\widehat p(1-\widehat p)$$
- Example:
	- Consider the previous situation. How large a sample is required if we want to be 95% sure that the error in using $\widehat p$ to estimate $p$ is less than 0.05?
	- $E=0.05$, $z_{\alpha/2}=z_{0.025}$, $\widehat p=0.12$, so $$n=\left(\frac{1.96}{0.05}\right)^2(0.12\cdot0.88)\approx162.269=163$$ 
	- So we need a sample size of 163.

### Approximate One-Sided Confidence Boundaries of Binomial Proportions
- The approximate $1-\alpha$ lower and upper confidence bounds are: $$\widehat p-z_\alpha \sqrt{\frac{\widehat p(1-\widehat p)}{n}}\le p$$ $$\widehat p+z_\alpha \sqrt{\frac{\widehat p(1+\widehat p)}{n}}\ge p$$ respectively.

### Guidelines for Constructing Continuous Intervals
- Most difficult step in constructing a confidence interval is often the match of the appropriate calculation to the objective of the study.
- Two primary comments can help identify the analysis
	1. Determine the parameter (and teh distribution of the data) that will be bounded by the confidence interval or tested by the hypothesis
	2. Check if other parameters are known or need to be estimated
![[Pasted image 20250630215440.png]]