### Recap
- We need `@staticmethod` and `@classmethod` decorators for static and class methods.
- Static methods don't require a pointer to `self`.

### Encapsulation
- We want to hide data and make things all nice and neat and work in the back end.
- We want private and protected attributes! We denote private attributes by a leading `__`, and we denote protected attributes by a leading `_`.
- So we can still just access private variables (or at least their values) through the `__dict__` method or `_ClassName__privateAttrivute`. This is a horrible design and the person who did it should be publicly executed.
- We really just have the *intention* of using at as a private attribute, it isn't a real one. Totally makes sense.
- Private attributes are only accessed from within the class.
- Protected attributes are accessed from within the class or its sub-classes.
- We can create private and protected methods as well. Sometimes Python isn't so terrible. Rare, but interesting scenario.

### Inheritance
- So derive a class from another by just passing the class names into the arguments of the new class definition.
- You can have multiple parents (GROSS)
- Go back and look at how things work. Class was slow and boring.

# Getters? Setters? Who don't `you.touch_some_grass`?