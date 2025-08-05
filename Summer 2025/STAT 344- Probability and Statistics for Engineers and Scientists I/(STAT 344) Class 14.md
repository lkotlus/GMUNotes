### Frequency Distributions
- A frequency distribution is a more compact summary of data than a stem-and-leaf diagram
- To construct, we must divide the range of the data into intervals, which are usually called class intervals, cells, or bins
- The number of bins is approximately equal to the square root of the number of observations
- Frequency distribution tables essentially just split the sample into bins and shows some stuff about them: 

|Class|$70\le x<90$|$90\le x<110$|$110\le x<130$|$130\le x<150$|$150\le x<170$|$170\le x<190$|$190\le x<210$|$210\le x<230$|$230\le x<250$|
|-|-|-|-|-|-|-|-|-|-|
|Frequency|2|3|6|14|22|17|10|4|2|
|Relative frequency|0.0250|0.0375|0.0750|0.1750|0.2750|0.2125|0.1250|0.0500|0.0250|
|Cumulative relative frequency|0.0250|0.0625|0.1375|0.3125|0.5875|0.8000|0.9250|0.9750|1.0000|

- Fairly easy to figure out that relative frequency is $\frac{n}{N}$, where $n$ is the frequency and $N$ is the number of elements. This essentially just makes it sort of like the probability of picking an element from the sample in that range, assuming you pick with an even probability.
- Cumulative relative frequency is just summing to the left, just like a CMF or CDF. 
- LCL: Lower Class Limit
- UCL: Upper Class Limit

### Histograms
- Just a visual display of the frequency distribution.
- Provides a visual impression of the shape and distribution of the measurements and information about the central tendency and scatter or dispersion in the data.
- Unequal bin widths will be employed. $$\text{height}=\frac{\text{bin freqeuncy}}{\text{bin width}}$$
- Constructing a histogram (equal bin widths)
	1. Label the bin boundaries on a horizontal scale
	2. Mark and label the vertical scale with the frequencies or the relative frequencies.
	3. Above each bin, draw a rectangle where the height is equal to the frequency (or relative frequency or cumulative frequency) corresponding to that bin.
- Mean: $\overline{x}$
- Median: $\widetilde{x}$
- So,
	- Negative/left skew: $\overline{x}<\widetilde{x}$
	- Positive/right skew: $\overline{x}>\widetilde{x}$
	- Symmetric: $\overline{x}=\widetilde{x}$
- A good measure of the center is the mean being equal to the median, a good measure of spread is the standard deviation.

### Box Plots
- The box plot is a graphical display that simultaneously describes several important features of a data set, such as center, spread, departure from symmetry, and identification of unusual observations or outliers.
- Sometimes called a box-and-whisker plot
- Displays three quartiles
- A line, or whisker, extends from each end of the box.
- The whisker extends to the smallest point within 1.5 interquartile ranges from the first quartile
- The first quartile is the left edge of the box
- The second quartile is the inner line in the box
- The third quartile is the right edge of the box
- The whisker extends to the largest data point within 1.5 interquartile ranges from the third quartile.
- Anything beyond the whisker is an outlier.
- Lower Fence (LF): $Q_1-1.5(IQR)$
- Upper Fence (UF): $Q_3+1.5(IQR)$
- Box plots can be vertical or horizontal

### Symmetric vs. Skewed Distributions
- Symmetric:
	- We use the mean and standard deviation for the center and spread measurements
	- $Q_1$ is equal distance from the median as $Q_3$. 
	- The min is equal distance from $Q_1$ as the max is from $Q_3$
	- The median line is in the center of the box in our box plot
	- The left whisker is the same length as the right whisker in the box plot
- Skewed:
	- We use the median and IQR for the center and spread measurements
	- Left:
		- $Q_1$ is further from the median than $Q_3$
		- Min is further from $Q_1$ than max from $Q_3$
		- Median line is to the right of the center of the box in our box plot
		- Left whisker is longer than the right whisker in our box plot
	- Right:
		- $Q_1$ is closer to the median than $Q_3$
		- Min is closer to $Q_1$ than max from $Q_3$
		- Median line is to the left of the center box in our box plot
		- Left whisker is shorter than the right whisker

### Time Sequence Plots
- A time series or time sequence is a data set in which the observations are recorded in the order in which they occur
- A time series plot is a graph in which the vertical axis denotes the observed value of a variable and the horizontal axis denotes the time
- Most intuitive graph ever.
- A digidot plot is a combination of a stem-and-leaf plot with a time series plot. The dots in the time sequence plot line up with their respective stems.