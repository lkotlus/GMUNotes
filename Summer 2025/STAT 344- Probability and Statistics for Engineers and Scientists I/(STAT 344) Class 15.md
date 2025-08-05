### Scatter Diagrams
- Multivariate: each observation consists of measurements of several variables
- The scatter diagram is a useful way to graphically display the potential relationship between two attributes of something
- We want to view a trend. Is it linear? Is it positive? Is it negative?
- When two or more variables exist, the matrix of scatter diagrams may be useful in looking at all of the pairwise relationships between the variables in the sample
- The sample correlation coefficient, $r$, is a quantitative measure of the strength of the linear relationship between two random variables ($x,y$): $$r_{xy}=\frac{\sum_{i=1}^n y_i(x_i-\overline{x})}{\left[\sum_{i=1}^n(y_i-\overline{y})^2\sum_{i=1}^n(x_i-\overline{x})^2\right]^{\frac{1}{2}}}$$
- Things to know: $$-1\le r\le 1$$
	- $r=1$: perfect positive correlation
	- $r=-1$: perfect negative correlation
	- $r=0$: no linear correlation, or nonlinear correlation
- The matrix of scatter diagrams essentially just has a diagonal of boxes that have measurements, and all other boxes are plots of the combinations of those measurements
	- Having both the upper and lower triangulars of this matrix is silly, as they are redundant.

### Probability Plots
- A probability plot is a graphical method for determining whether sample data conforms to a hypothesized distribution based on a subjective visual examination of the data
- To construct a probability plot:
	- Rank the data observations in the sample from the smallest to largest
	- The observed value $x_j$ is plotted against the observed cumulative frequency $\frac{(j-0.5)}n$
	- The paired numbers are plotted on the probability paper of the proposed distribution
- If the hypothesized distribution adequately describes the data, the plotted points will fall approximately along a straight line.
- If the plotted points deviate significantly from a straight line, then the hypothesized model is not appropriate
- Normal Probability Plot
	- Can be constructed on ordinary axes by plotting the standardized normal scores $z_j$ against $x(j)$, where the standardized normal scores satisfy: $$\frac{j-0.5}{n}=P(Z\le z_j)=\Phi(z_j)$$