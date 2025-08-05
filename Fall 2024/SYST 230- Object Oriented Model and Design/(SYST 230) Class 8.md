### Class relationships!
- Aggregation, composition, and whatnot.
- Examples:
	- Generalization, "subclass is a superclass" (blank arrow)
	- Composition, "system has a part" (black diamond, stronger than below)
	- Aggregation, "system has a part" (white diamond)
	- Association, "uses" (just a line)
	- There's more, but we didn't go into it.
- These can be bidirectional with use of a baby arrow thingy

### Composition vs. Aggregation
- An aggregate relationship is one where if you delete the system, the parts will remain.
	- Part objects are created outside the system object.
- A composite relationship is one where if you delete the system, the parts are also deleted.
	- Part objects are created within the system object.
