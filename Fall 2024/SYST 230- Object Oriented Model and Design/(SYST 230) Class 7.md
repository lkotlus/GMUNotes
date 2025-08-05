### Quick recap
- We can have private and protected attributes with a leading `__` and `_` respectively.
- Python still lets you grab it from the namespace. Gross.
- It's really just an indication that you're trying to use it a certain way.
- Private methods of a parent class must be called through methods inherited through the parent class.
- If we method override, we cannot access the old method.
- We must provide `self` if we use `ParentClassName.__init__(self, ...)` for calling a super constructor. Not the case if we do `super().__init__(...)`.

### UML
- Boxes and arrows, homeskillet.
- Class diagram:
	- Arrows point from children to parents
	- Rectangle with sections.
		- Class Name
		- Attributes
		- Methods
	- Attributes and methods are prepended with a + if public, - if private, and # if protected.