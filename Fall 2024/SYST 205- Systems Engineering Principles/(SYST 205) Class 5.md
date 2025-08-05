### More functional diagrams with IDEF0!
- Viewpoint matters!
- Students, instructors, and the CEC will all have different inputs, controls, outputs, and mechanisms for a "succeed in SYST 205" function.
- We **must** remove our bias when doing this.
- Decomposition goes until we find something atomic (doesn't need to be split into parts). 
- On an exam, let's save ourselves work. Three boxes. "Do 2 levels of decomposition" can lead to 26 boxes! It's only 13 if we do 3 on each level.
	- **<u>Sanctioned by the professor</u>**

### Activity diagrams!
- Top to bottom logical flow of activities through time (but not at any particular time).
- In-sequence activities occur after each other. Activities that could occur together will go parallel, although they might take different amounts of time and start at different times.
- Decision logic is here. Decisions are always binary!
- Decisions are diamonds and are a version of true or false based on the present conditions. If the question can't be answered true or false, you haven't asked the right question. We can technically nest things.
	- Say we wan't to know if we are even, odd, or prime.
	- Check for even/odd first, then check for prime under both trees (technically just x=2 for the even nest). 
	- The prime paths join together, and then even/odd paths remain separate.
- DO NOT:
	- Have three decision outputs
	- Have a line as a join from decisions.

### State Modeling!
- Represent the life cycle of a block
- Supports event-based behavior (generally asynchronous)
- Event types:
	- Change event
		- Event that represents a condition.
		- Condition is defined by a boolean valued expression that triggers a transition when its value changes to true.
		- Example: turn key in ignition
	- Time event
		- Event that represents the passage of a defined period of time or an absolute time.
		- Example: lights in car turn off after 15 seconds of the car being off
	- Signal event
		- A specific message that initiates a transition when an object receives it.
		- Example: engine changes from idle to acceleration when foot is put on gas

