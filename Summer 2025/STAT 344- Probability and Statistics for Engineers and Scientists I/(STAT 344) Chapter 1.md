## Learning Objectives
1. Identify the role that stats can play in engineering
2. Discuss how variability affects the data collected and used for making engineering decisions
3. Explain the difference between enumerative and analytical studies
4. Discuss teh different methods that engineers use to collect data
5. Identify the advantages that designed experiments have in comparison to other methods of collecting engineering data
6. Explain the differences between mechanistic models and empirical models
7. Discuss how probability and probability models are used in engineering and science.

## Intro
- Stats is a science that helps us make decisions and draw conclusions in the presence of variability.
- We use stats for everything from systems planning to engineering. Emergency room visits to machine learning.

## The Engineering Method and Statistical Thinking
- The steps of the engineering method:
	1. Develop a clear and concise description of the problem
	2. Identify, at least tentatively, the important factors that affect this problem or may play a role in its solution
	3. Propose a model for the problem, using scientific or engineering knowledge of the phenomenon being studied. State any limitations or assumptions of the model.
	4. Conduct appropriate experiments and collect data to test or validate the tentative model or conclusions made in steps 2 and 3.
	5. Refine the model on the basis of the observed data.
	6. Manipulate the model to assist in developing a solution to the problem.
	7. Conduct an appropriate experiment to confirm that the proposed solution to the problem is both effective and efficient.
	8. Draw conclusions or make recommendations based on the problem solution.
- Collecting and refining data plays a huge role in this.
- Statistics deals with the collection, presentation, analysis, and use of data. This makes it naturally very helpful for engineers and scientists based on the above engineering/scientific method.

### Variability
- Statistical methods are used to help us describe and understand **<u>variability</u>**.
- Variability:
	- Successive observations of a system or phenomenon do not produce exactly the same result.
- Statistical thinking can give us a useful way to incorporate this variability into decision making.
- Different factors in a situation are called ***sources of variability***.
- If a measurement exhibits variability, we consider it to be a <u>**random variable**</u> ($X$ is the variable, $\mu$ is constant, and $\epsilon$ is a random disturbance): $$X=\mu+\epsilon$$

### Populations and Samples
- A <u>**sample**</u> is a grouping of data from a <u>**population**</u>.
- Mapping results from a sample to the population is called <u>**statistical inference**</u>.
- Initially, measurements were taken from populations of actual people. This is why we have terminology that sticks. A bad sampling leads to misleading data.

## Collecting Engineering Data

### Basic Principles
- Data that is all of the observations in the population results in a ***census***.
- We almost always use a ***sample*** instead.
- Three basic methods of collecting data:
	1. Retrospective study (using historical data)
	2. Observational study
	3. Designed experiment
- Effective data-collection greatly simplifies analysis.

### Retrospective Study
- We take historic data and observe that rather than creating new data.
- The main problem with this is that historic data doesn't necessarily have the measurements we want.
- Retrospective studies have a significant amount of data, but it might not contain much useful information. There might be outliers that result from poor book-keeping, as well.

### Observational Study
- Observe the process/population, disturbing it as little as possible and recording quantities of interest.
- Usually conducted for a relatively short time period, so some variables that aren't routinely measured can be included. 
- Observational studies tend to help get reliable data that has the information we want, but can't stop the way that things are performed from being different from how we want to observe them.

### Designed Experiments
- Deliberate or purposeful changes in the controllable variables while observing.
- Experiments designed with basic principles such as <u>**randomization**</u> are needed to establish <u>**cause-and-effect**</u> relationships.
- 