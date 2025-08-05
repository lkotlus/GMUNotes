### Coming to the end of the semester
- Next two to three weeks are the last core lectures, after that we'll be focusing on final prep.
- Course work is pivoting into just the semester project.

### System of systems (SoS) engineering
- Similar to IDEF0, perspective matters.
- There is subtlety in saying what is a system within an SoS.
- International air travel!
	- There is an SoS for this.
	- We say there is an SoS because there isn't a single body in charge of this. Each country is sovereign in respect to its airspace.
- Is GMU a system or an SoS?
	- From the perspective of the students seeking education, is GMU a system, or an SoS?
	- The real question is if there is a sole arbiter within this that is the one in charge. Lower the scope to the College of Engineering and Computing (CEC), and the dean isn't the guy optimizing everything. It is a department strucuture. CS department and CYSE department are separate systems.
	- It is a federation of systems, not a monolithic system.
- US government!
	- SoS
- Healthcare E-records example:
	- INOVA, UVA, and VHC are all hospitals in VA.
	- Let's assume that each INOVA hospital uses the same software for records. 
	- I go to INOVA hospitals. When I'm at UVA hospitals, how do they get my health records?
	- Well, we agree on this neutral party (Health Information Exchange, HIE), then we can all send our data there and get data from there. It doesn't matter what we do locally, it just matters what we do with them.
		- To communicate with this other party, we need an agreed upon language. In engineering, we call this agreed upon language for different parties a <u>standard</u>. Just like how my phone and AirPods know that they are using the Bluetooth standard.
	- The point of the system we use with HIE is that to me it looks like a single integrated whole system. But in reality, it's a complex SoS. 
- The Apple ecosystem!
	- We have the:
		- iPhone
		- iPad
		- Apple TV
		- Macbook
		- iMac
		- Apple Cloud
		- iMessage
		- iTunes
	- We want to say SoS, but it could just be a bunch of individual systems that work well together as the ecosystem. 
	- The tight integrations are evidence of governance, because if left to their own devices we just had to sell as many iMacs as possible, then we wouldn't care about targeting iPhone users.
	- We are trying to create an integrated system that adds incentive to continue to purchase products within it.
	- If the only goal is to sell AirPods, we don't sell to iPhone users specifically. But really, we're selling the whole system.
	- There is intentionallity of design within each subsystem.
- Standard/regulatory bodies are not enough to define a system. We must also see optimizations being made at that level.

### Activity diagrams (again)
- Lovely.
- We modelling three discrete activities, each with at least two decisions and splits.
- **<u>Taking something, turning it into an IDEF0, and turning that IDEF0 into an activity diagram has been on the final for this class before.</u>**

### State diagrams
- The intimate connection between my brain and a railroad spike is crazy rn.
- "State diagrams are conceptually one of the more difficult things in this class."
	- This feels like cap.
- State diagrams
	- Typically used to represent the life cycle of a block
	- Supports event-based behavior (generally asynchronous)
	- Event types
		- Change event:
			- Represents a condition.
			- Condition is defined by a boolean-valued expression that triggers a transition when its value changes from false to true (e.g. turn key in ignition)
		- Time event:
			- Event that represents the passage of a defined period of time or an absolute time.
			- A transition with a time event trigger initiates when the time value is satisfied (e.g. lights in car turn off after 15 seconds of the car being off)
		- Signal event:
			- A specific message that initiates a transition when an object receives it (e.g. engine changes from idle to acceleration when foot is put on gas)
	- Interesting, I guess.
	- We have sinks and starts and whatnot. Squircles are states, we can have states within states. 
	- Triggers:
		- `trigger[guard]/action`
		- Trigger name, requirement for the trigger, resulting action from the trigger.
		- Example: `start[in neutral]/start engine`
		- The trigger is start, you must be in neutral to start a car, and the action is starting the engine.
	- THINK ABOUT THESE BEFORE MAKING THEM!!!!