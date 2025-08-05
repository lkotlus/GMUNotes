### Quiz and administrative information
- I thought I had an 80 something, but I really got a 92.5. Built-in extra credit, graded out of 40 rather than 45.
- Not telling me this is criminal, makes me want to cry to death.
- So once we have a design, we can write the code however we'd like. It's good practice to comply with the design.

### Special (Magic or Dunder) Methods
- Define the `__str__` method, and we can cast our objects to strings with the `str()` method. Kwazy.
- Difference between `__str__` and `__repr__` is that `__repr__` is useless and doesn't do much of anything at all. The only purpose of `__repr__` is to help fellow grammers understand what you're doing. Typically, you show how it was constructed.
- If there is no `__str__` method, then `__repr__` is going to be called. 
- The `sorted` method in an array is going to depend on things like `__lt__` being implemented in your objects.

### IPython Magic Commands
- JupyterNotebook silliness
- Just random stuff with `%` before the command.
- Very silly.

### The `@property` decorator
- We can put this over a method and we will be able to get it as if it's an attribute.
- No more need for getter syntax.
