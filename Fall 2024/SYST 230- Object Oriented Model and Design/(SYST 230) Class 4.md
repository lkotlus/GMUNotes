## Objects and Whatnot
- An object is an instance of a class. We will use "object" and "instance" interchangeably.
- Instance vs. Class Attributes:
	- Instance Attributes: accessible only by an instance of the class
	- Class Attributes: accessible by every instance of the class
- Namespace:
	- Anything you do within a class is inside the namespace. If I call a method from an instance and I get an error, then the issue is because the method is not defined within the namespace. 
	- Each object has it's own namespace as well.
	- It's the unique address/ID of the class.
	- The `__dict__` attribute shows the namespace of a class or object as a dictionary.
- Instance vs. Class Method:
	- Class methods we just normally define within our class.
	- Instance methods are the ones with dunders (double underscores)
- Class attributes in python are defined outside of the `__init__` method.
- When you attempt to modify a class attribute in python, it will create an instance attribute of the same name with a new value.
- If we have a dictionary with the same keys and values as our attributes, the we can just use `setattr()` and `getattr()`. 
- So in the following scenario, we have these class and dict definitions:
```python
class Person:
	def __innit__(self, first=None, last=None, pay=None):
		self.first = first
		self.last = last
		self.pay = pay

person_info = {'first': 'Lee', 'last': 'Majors', 'pay': 78000}
```
- This means we just need to do this with `setattr`.
```python
person = Person()

for key in person_info.keys():
	setattr(person, key, person_info[key])
```
- So exciting...
- Well, let's say we want to do this like not big dumb idiots. We'd just use fancy python notation:
```python
person = Person(**person_info)
```

### End of class challenge (this is the easiest thing that I have ever seen in my life, it was like 15 minutes of class silence before I answered it smh my head rn now fr real)
- Take the following dictionary, and create a new one `student_info2` with Objects instead of dictionaries as values.
```python
student_info = {
'G001': {'first': 'Lee', 'last': 'Majors', 'CGPA': 2.5},
'G002': {...},
'G003': {...},
...
}
```

- This is just code we wrote earlier inside a for loop. This is not hard. The only hard thing is resisting the urge to ram my head through a railroad spike rn now.
```python
student_info2 = {}

for i in student_info.keys():
	student_info2[i] = Person(**student_info[i])
```