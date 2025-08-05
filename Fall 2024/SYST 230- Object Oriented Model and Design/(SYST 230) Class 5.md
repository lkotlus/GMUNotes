We might learn some OOP today, isn't that crazy?

## More on objects
- The `setattr()` method has more uses than we know currently, we will learn more.
- The `self` attribute references the instance. If you use a reference with the `ClassName`, then you will always reference class attributes. This makes sense, rare Python W.
- Classic class attribute example with an instance counter.
- World record time of being told to stop answering questions in only 28 minutes of lecture! I deserve an award for this fine achievement.
- Prediction: `x = x+1` creates a new object, `x += 1` updates the current object. The `+` operator returns a new object, so this makes sense. Python is horrible.
- My prediction is correct. The `+=` operation is in-place, whereas `+` returns a new object.
- Class methods! We need an `@classmethod` decorator before the method definition in order for the interpreter know it is a class method. Makes sense, but maybe the genius developers of Python should have made a language with real syntax so I don't need to do things like this. Ridiculous.
	- A class method literally just takes a reference to the class as its first parameter rather than a reference to the object/instance.
- For convention, we use `cls` instead of `self` in a class method.
- Interesting example with what is essentially a method override for the constructor:
```python
@classmethod
def from_str(cls, emp_str):
	first, last, pay = emp_str.split('-')
	return cls(first, last, pay)
```
- Pretty legit.
- "That's what happens when you are old."
- Static methods! Guess what... `@staticmethod`! I can't stand the decorator syntax, so uggo. 
- Dunder methods! We have the built in functions that we want to use like `__len__` and `__str__`. 