### Warm Up
- Future populations of rabbits ($R$) and foxes ($F$) over time ($t$, in years) are modeled as such: $$\frac{dR}{dt}=3R-1.4RF\ \ \ \ \ \ \ \frac{dF}{dt}=-F+0.8RF$$
- In earlier work, assumed only one species, unlimited resources, and species reproduced continuously. Which, if any, of these assumptions is modified and how is this modification reflected in the above system.
	- We have two species, limited resources for foxes, and variable reproduction for foxes.
- Interpret the meaning of each term in the rate of change equations. 
	- $3R$ is the continuous rabbit reproduction
	- $-1.4RF$ is the decrease in rabbit population from foxes hunting
	- $-F$ is foxes dying of starvation
	- $0.8RF$ is foxes reproducing to their ability from the presence of rabbits

### Systems of Differential Equations
- I love linear algebra!
- We can always just do numerical methods for these things.
- With our rabbit and fox model from above, we can do Euler's method:

|$t$|$R$|$F$|$\frac{dR}{dt}$|$\frac{dF}{dt}$|
|-|-|-|-|-|
|0|1|1|1.6|-0.2|
|0.5|1.8|0.9|3.132|0.396|
|1.0|3.366|1.098|N/A|N/A|
