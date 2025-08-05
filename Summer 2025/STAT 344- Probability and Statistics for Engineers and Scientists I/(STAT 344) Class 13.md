### Descriptive Statistics
- Outline.

### Numerical Summaries of Data
- Data summaries and displays are essential to good statistical thinking
- It is useful to describe data features numerically
- Characterizing the location or central tendency in the data is an example of a numerical summary
- Data are often a sample of observations that have been selected from some larger population of observations
	- This type of population is called a conceptual or hypothetical population, because it does not physically exist
- Sample mean
	- The location or central tendency in the data can be characterized by the arithmetic average or the sample mean: $$\overline{x} = \frac{\sum_{i=1}^{n} x_i}{n}$$
	- For a finite population with $N$ equally likely values, the PMF is $f(x_i)=\frac{1}{N}$ and the mean is: $$\mu=\overline{x}$$
	- Literally just divide the sum by the number of elements.
- Sample Variance and Standard Deviation
	- The variability or scatter in the data may be described by the sample variance or the sample standard deviation: $$s^2=\frac{\sum_{i=1}^n(x_i-\overline{x}^2)}{n-1}$$
	- We can also use a shortcut: $$s^2=\frac{\left(\sum_{i=1}^nx_i^2\right) - \frac{1}{2}\left(\sum_{i=1}^nx_i\right)^2}{n-1}$$
	- $n-1$ compensates for error from basing calculations on $\overline{x}$ rather than $\mu$
- Degrees of Freedom
	- When the sample variance is calculated with the quantity $n-1$ in the denominator, the quantity $n-1$ is called the degrees of freedom.
	- Origin of the term:
		- There are $n$ deviations from the $\overline{x}$ sample
		- The sums of the deviations is zero
		- $n-1$ of the observations can be freely determined, but the $n$th observation is fixed to maintain the zero sum
- Sample Range
	- In addition to the sample variance and sample standard deviation, the sample range is a useful measure of variability. $$r=\max(x_i)-\min(x_i)$$
	- So just the difference between your max and min.

### Stem-and-Leave Diagrams
- Steps to construct an Stem and Leaf Diagram:
	1. Divide each number $x_i$ into two parts: a stem, consisting of one or more of the leading digits, and a leaf, consisting of the remaining digit
	2. List the stem values in a vertical column
	3. Record the leaf for each observation beside its stem
	4. Write the units for the stems and leaves on the display
- This helps to visualize the data in a very easy way.