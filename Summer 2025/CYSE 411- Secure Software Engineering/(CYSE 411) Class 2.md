### Software Development Lifecycle
- This is the base of the whole course!
- What is Software Engineering (SE)
	- Branch of computer science that deals with designing, developing, testing, and maintaining software applications.
	- Maintainability: software should be written so that it can evolve to meet the changing needs of customers.
	- Dependability and security: software dependability includes a range of characteristics, including reliability, security, and safety. Dependable software should not cause physical or economic damage in the event of system failure.
		- Have threats without risk!
	- Efficiency: don't make wasteful use of system resources. $\text{O}(n\log(n))$ for your sorting algorithms, no bubble sort.
	- Acceptability: software must be acceptable to the type of user it is designed for. UI design technically matters.
- Software development fails when we:
	- Don't deliver the product
	- Don't have the budget
	- Don't meet the deadline
	- Don't have the correct people
- Only 20% of the software's existing functionalities generate value to the product. Only 20% of what is really needed is unknown at the start of the product. 60% code waste means we pay for trash.
- Enter the SDLC
	- What we're doing:
		- Planning
			- Perform requirement analysis. Customer input and sales department/market surveys. Figure out the problem that we're solving.
		- Requirement Defining
			- All the requirements for the target software are specified. SRS (Software Requirement Specification) is performed. 
		- Designing
			- SRS is a reference for the developers to create the best architecture for the software. We are designing that architecture in this phase, and we put those into the DDS (Design Document Specification).
		- Building
			- Fundamental development of the product starts. Specific languages are chosen per the DDS.
				- Development
				- Coding Standard
				- Scalable Code
				- Version Control
				- Code Review
		- Testing
			- At this stage, all probable flaws are tracked, fixed, and retested. Ensures that the product confronts the quality requirements of the SRS. Unit tests are actually part of the code today.
				- System Testing
				- Manual Testing
				- Automated Testing
		- Deploying and Maintaining
			- Actually sending stuff out
				- Deployment and Maintenance
				- Release Planning
				- Deployment Automation
				- Maintenance
				- Feedback
- Waterfall Model
	- We have:
		- Requirements Definitions
			- System and Software Design
				- Implementation and Unit Testing
					- Integration and System Testing
						- Operation and Maintenance
	- The problem is that each phase is separate. We can only see a problem when we reach that phase. If I find a problem during the testing phase with the requirements then we need to go all the way back.
	- Sequential approach: we go one by one
	- Document-driven: each phase generates a document
	- Quality control: high emphasis on this
	- Rigorous planning: we need a very careful definitions phase to not get backlogged
	- Overall, not great for modern day software development.
		- No feedback path
		- Difficult to accommodate change
		- No overlapping of phases
		- Limited flexibility
		- Limited stakeholder involvement
		- Late defect detection
		- Lengthy development cycle
- Cost of Change (Barry Boehm)
	- The further along in the project we are, the higher the cost of change.
- Iterative model
	- We repeat the waterfall (sometimes starting at design) until the project is finished.
	- Each cycle results in a semi-developed but deployable version. With each one, some requirements are added to the software.
	- We can make changes and see issues much faster.
	- Disadvantages:
		- Higher complexity
		- Unsuitable for small projects
- Spiral model
	- Imagine a spiral going clockwise through four quadrants. 
		1. Identify Objectives
		2. Risk Analysis
		3. Product Development
		4. Evaluation
	- One of the most crucial SDLCs that support risk handling.
	- Disadvantages:
		- Management is more complex
		- The end of the project may not be known early
		- Not suitable for small and low-risk projects
		- The spiral may go indefinitely
		- A ton of intermediate stages that lead to excessive documentation
- V-Model
	- Executed sequentially
	- Each stage or phase is integrated with a testing phase
	- Also known as the verification or validation model.
	- We can adapt to issues far sooner
- Agile Model
	- Designed to adapt to changing requests quickly. Facilitates quick project completion. Agile refers to a group of development processes.
	- Manifesto for agile software developers:
		- Individual and interactions over processes and tools
		- Working software over comprehensive documentation
		- Customer collaboration over contract negotiation
		- Responding to change over following a plan.
	- 12 Agile Principles
		1. Satisfy the customer
		2. Welcome change
		3. Deliver frequently
		4. Work together
		5. Trust and support
		6. Face-to-face conversation
		7. Working software
		8. Sustainable development
		9. Continuous attention
		10. Maintain simplicity
		11. Self-organizing teams
		12. Reflect and adjust
	- This is the most important one (according to our professor).
- SCRUM
	- FBI Sentinel Project
		- FBI awarded Lockheed Martin a contract to develop the Sentinel System
		- A quarter of the budget was spent on planning
		- Big promises, but they went way over budget. 
		- Someone used Agile and did it way better.
			- Used a quarter of the budget
			- Design broken into 670 user stories
			- Iterative development
			- Self-organizing teams
	- SCRUM is a project management framework that helps teams structure their work and deliver projects efficiently. It's an agile framework. Centered around:
		- Commitment: team members agree to complete tasks that they can
		- Courage: team members question the status quo
		- Accountability: teams emphasize accountability and iterative progress
		- Communication: teams encourage good communication
	- We want to:
		- Self-organize teams
		- Create series of 1-4 week "sprints"
		- Requirements are captured in "product backlog"
		- No specific engineering practices are prescribed
		- Uses generative rules to create an agile environment
		- One of the "agile processes"
	- Every 2-4 weeks we have a sprint. There's a goal for every sprint, which is taken from the product backlog. This generates a sprint backlog, which is just the list of each thing we need to get done to deliver the sprint goal. Every day we have a SCRUM meeting. At the end of the sprint, we increment. 

### Things to do
- Watch the SCRUM video (unit 1.2).
- You need to log in to the GitHub student thing.
- Assignment 1
	- Assignment steps are in the README file.
	- Just do the GitHub stuff
- Quiz 1
	- You will have a week to complete it after it is released
	- No cheat sheet
	- Make sure your Windows VM is working