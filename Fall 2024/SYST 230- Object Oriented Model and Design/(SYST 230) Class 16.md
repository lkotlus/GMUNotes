### Switching to SysML
- Quiz 3 is going to be all adding things to a base model that we will begin working on today!
- We're doing SysML now, which is a bit better for systems that involve physical attributes.
- Some SysML diagrams are a bit different from UML, and two diagrams aren't present at all:
	- Requirements diagram
	- Parametric diagram
- SysML is a system framework for designing:
	- Mechanical design models
	- Electrical design models
	- Software design models
	- Testing methods and models
- SysML provides:
	- External requirements
	- System documentation and specifications
	- Analysis needs
- Blocks
	- The block is the modular unit of structure in SysML that is used to define a type of system, component, or item that flows through the system.
	- A block is defined by the features it owns, which may be divided into structural and behavioral features
	- A block is a type or a set of similar instances, or objects, all of which exhibit common characteristics (class)
	- The meaning of a block can be a type of logical or conceptual entity, a physical entity; a hardware, software, or data component; a person; a facility; an entity that flows through the system; or an entity in the natural environment (it can be anything)
	- Blocks are essentially just classes!
- Blocks vs. Classes:
	- A block has the following property types: constraint, flow, part, reference, and value. It also has operations, just like a class.
	- Parts are true physical things that aren't just values. For example an ATM has:
		- CPU
		- Display
		- etc.
	- Values are things that are actually values that are stored. Continuing the ATM example:
		- Weight
		- Available cash
		- etc.
	- Operations are just functions:
		- Get balance
		- Verify user
		- etc.
	- Everything is public in a block!
- Block compartments:
	- We can make parts and values all composite relationships
	- Parts are all other blocks, values are `<<valueType>>`.

|bdd|\[Package\]|Structure|\[Structure\]|
|-|-|-|-|
|Diagram Type|Owner Type|Owner Name|Diagram name|

- Very cool.
- Some stuff:
	- In SysML we think of definition, usage, and instance/object.
	- Definition is our block diagram, usage is the names and whatnot, and an instance (or object) is just like an instance of a class.
- Neat.
- If you have two parts of the same type, then you have two composition relationships to the same block. <u>Each one has a different name!</u>