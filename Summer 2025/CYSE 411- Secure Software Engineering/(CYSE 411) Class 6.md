### System Modeling
- Goal
	- Understand and apply threat modeling techniques to identify, evaluate, and mitigate security risks during the system design phase.
- What is threat modeling?
	- A process by which potential threats, such as structural vulnerabilities or the absence of appropriate safeguards, can be identified and enumerated, and countermeasures prioritized.
	- This analysis helps identify security risks and inform protective strategies
	- About using models to find security problems. This whole process aids with learning about the system.
- Threat modeling process
	 1. System modeling
	 2. Threat enumeration
	 3. Ranking threats
	 4. Countermeasures and mitigations
	 5. Repeat
- Threat modeling and SDLC
	- Threat modeling evaluates a system from the attacker's perspective rather than the defender's
	- We do our threat modeling in the design phase
- Why do we model?
	- What is a model?
		- A model is an informative representation of an object, person, or system
		- An abstraction of a complex system to a certain level
			- To a certain level, because we don't necessarily need to see if we have setters and getters for methods in the design phase. It just doesn't matter for the level of detail we're going for.
		- Any type of diagram from SysML, UML, etc.
	- Why do we model?
		- The original system is too complex for human beings to comprehend
		- We model a system with a specific focus to a particular detail level such that we can better understand the system
- Levels of abstraction
	- What level of abstraction must be applied when we model? Depends on the needs.
		- If we want to study DDoS attacks, we might just need each computer/router as a node.
		- If we want to study hardware-related attacks, we may safely neglect to model the OS
		- If we want to study buffer overflows, we might need to consider both the OS and memory
- George Box said that:
	- "All models are simplified abstractions; their value lies in how well they help us understand complex systems."
	- Essentially, all models are wrong.
- Models can be incomplete or inaccurate:
	- Incompleteness (under this context)
		- It does not refer to the nonessential parts that were intentionally left out
		- Refers to the important ones that should have been included
		- Causes of incompleteness
			- Incompleteness can be caused by a security engineer's limited knowledge space, unintentional negligence, etc.
			- For example, someone models a product's security threat model but fails to consider supply-chain attacks on chip manufacturers or libraries.
	- Inaccuracy
		- The model of a system may not accurately reflect the real system that is up and running.
			- The design process is complex, and discrepancies can be introduced in many ways at many locations
			- A system is constantly under change by the owner and operation, which the model may not necessarily reflect.
- Defender vs. Attacker Perspectives
	- While defenders control the system - a significant advantage - they face a daunting challenge: they must identify and protect against every possible vulnerability
	- In contrast, attackers only need to find and exploit one weak point to succeed
	- Attackers also benefit from the element of surprise: they choose when, how, and where to launch their attack
	- Through recon, an attacker's understanding of the system can sometimes be as complete - or even more accurate - than the defender's
- Shostack's Four Question Framework:
	1. What are we working on?
	2. What can go wrong?
	3. What are we going to do about it?
	4. Did we do a good enough job?
- Fundamentals:
	- Focusing on assets
		- Start modeling by focusing on assets
		- The three types of assets:
			1. Things attackers want (PII, passwords, etc.)
			2. Things you want to protect (reputation, faith, etc.)
			3. Stepping stones to either 1 or 2 (network, memory, CPU, etc.)
	- Focusing on attackers:
		- Start threat modeling enumerating either real or hypothetical hackers
			- Intensive and incomplete
			- Still a bottom-up approach
			- Can easily get subjective and/or miss the big picture
	- Focusing on systems:
		- Focus on the software being built or the system being deployed
			- The most common approach
			- Can be built based on design documents, which are usually accessible
			- Flexible and can accommodate asset change
	- Diagrams:
		- Diagrams are an excellent way to communicate what you are building
		- You can use a simple whiteboard to design your system
		- Data flow diagram (DFD):
			- A DFD maps out the flow of information for any process or system
			- This is the diagram for security users. It's the one that we use the most.
			- Diagram components:
				- External entity: outside systems that send and/or receives data, communicating with the system being diagrammed (rectangle)
				- Process: any process  that changes the data, producing an output. It might perform computations, sort data, or direct the data flow. (squircle)
				- Data store: files or repositories with information for later use, such as a database (parallel lines)
				- Data flow: the roue data takes between the external entities, processes, and data stores (arrows)
				- Trust boundary: surrounds the system in different layers (dashed rectangle)
- Example: Pet Web System
	- The pet web system is an e-commerce application that sells pet items (food, toys, etc.). To buy an item, the client must have an account, log in, and access a wallet.
	- Identify use-case scenarios:
		- Understand the context of the problem that you want to design the security for
		- Evil user stories or security stories help define this
		- Use a brainstorming process
		- Examples:
			- User story: As a client, I want to buy items from the pet web system so I can care for my pet
			- Evil user story: As an attacker, I want to access the database to steal credit card information
			- Security story: As a sysadmin, I want to use an external payment gateway to avoid transactions being compromised
		- Ask about system design decisions for the system architecture
		- Ask about constraints to stakeholders
		- Check which type of architecture the system uses
			- We use a 3-tier architecture
				 1. Web server
				 2. Business logic
				 3. Data store
	 - DFD Walk through:
		 - Define system boundaries
			 - Identify scope
				 - Determine the boundaries of the system you're analyzing
				 - This includes identifying the components, external entities, data stores, and data flows within the system
				 - Take care about what is essential
				 - What the system must perform?
					 1. See items on the catalog
					 2. Add items to the wallet
					 3. make a payment
					 4. Register the transaction
					 5. confirm the transaction was successful
				 - Who performs the above actions?
					 1. Web client (1, 2, 3, 5)
					 2. Payment gateway (3, 5)
					 3. Database (4)
				- Determine trust boundaries
					- Understand the boundaries between trusted and untrusted components
					- Show where data crosses from one level of trust to another. This is crucial for identifying security concerns.
					- Entry points define the interfaces to which potential attackers can interact or supply the application with data
						- Entry points show where data enters the system 
						- Exit points are where it leaves the system
						- Entry and exit points are always WITHIN the system boundary. You can tell what they are based on directions of arrows. 
							- Arrow going into the system boundary: entry
							- Arrow coming out of the system boundary: exit
							- Both: both
		 - Identify external entities
			 - Identify all external entities that interact with the system. These could be users, other systems, or external services.
			 - Understand interactions. For each external entity, understand how they interact with the system, specifically what data they send to or receive from the system.
			 - Identify interactions for each external entity
		 - Identify processes
			 - Identify all the processes that handle data within the system. These processes can include functions, microservices, or any operation that processes the data
			 - Describe each process:
				 - Document what each process does and how it handles data, including any transformations or logic applied to the data.
				 - User verbs!
			 - Put each process within their trust boundary
		 - Identify data stores
			 - List data stores:
				 - Identify all data stores within the system. Databases, file systems, caches, etc.
		 - Identify data flows
			- Map data flows:
				- Understand how data flows into and out of each data store and which processes read from or write to these stores
		 - Label flows and trust boundaries
			 - Clearly label each data flow with the type of data being transferred, such as user credentials, personal data, config files, etc.
		 - Finalize the DFD
			 - Check the correct use of standard symbols
			 - Layer the DFD
				 - Depending on complexity, you might create a high-level (context) DFD and then break it down into more detailed DFDs for each subsystem
- Creating a DFD:
	- Use Project Threat Dragon
- Diagram validation
	- Any time you find someone saying "sometimes" or "also," you should consider adding more detail to break out the various cases
	- Any time you need more detail to explain security-relevant behavior, draw it in
	- Each trust boundary box should have a label inside it
	- Anywhere you disagreed over the design or construction of the system, draw in those details
	- Don't have data sinks: you write the data for a reason - show who uses it
	- Data can't move itself from one data store to another, show the process that moves it
	- If there are mechanisms for controlling data flows (such as firewalls or permissions), they should be shown
	- All processes must have at least one entry data flow and one exit data flow
	- Diagrams should be visible on a printable page