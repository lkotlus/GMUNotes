Maybe people will know how Python works this time... but probably not.

## Class start

### Pre-lecture
- "Some students talk a lot"
	- Okay, shots fired.

## Mutable Versus Immutable Data Types

### Example
```python
# Allowed (lists are mutable)
a = [1, 3, 3]
a[1] = 2

# Not allowed (tuples are immutable)
a = (1, 3, 3)
a[1] = 2
```

### What's the big idea?
- Mutable (can be mutated) data types support reassignment of specific elements.
- Immutable (can't be mutated) data types do not.
- That's the whole thing, but it does have funky implications...
- This guy has named a string variable `str` in an object-oriented Python course. My brother in Christ, that is the class name for strings, you are creating conflicts!
- Note: everything is a pointer, so the variable can be changed but the object it points to cannot be. This is useful, but also a nightmare sometimes. 
- Make sure we know if a method is working in-place or returning a mutated object. 

### Copying our objects
- Shallow vs. Deep Copy
	- Shallow copy just means we have a pointer to the same object. This is fast but annoying.
	- Deep copy means we have created a new object in memory that is identical (in content) to the original. This is slow and expensive.
- This makes things even more complicated when we include mutable vs. immutable. Here's the rule:
	- Immutable: always a deep copy (`tuple1 = tuple2 // deep`)
	- Mutable: always a shallow copy (`list1 = list2 // shallow`)
- Some methods of fake deep copying mutable data types (that aren't nested):
	- `b = [i for i in a]`
	- `b = a.copy()` 
	- `b = a[:]`
- The above examples aren't technically deep copying because they do not deep copy the elements inside.
- Some methods of deep copying mutable data types that are nested:
	- We need to be total nerds about it and write some recursive/known-depth method that will copy every object within every object. See below:
	```python
	def deepCopyList(l):
		lcp = []

		for i in l:
			if (isinstance(i, list)):
				lcp.append(deepCopyList(i))
			else:
				lcp.append(i)

		return lcp
	```
	- If you don't want to write it yourself, `import copy`.

### Mutable objects and functions
- All other languages either do argument by value or argument by reference
	- By value: you use a copy of the value (local to the function)
	- By reference: you use a pointer of the value (points to the other variable)
- Python does neither, because it is a special little boy.
- It does pass by object
	- So you pass your object in rather than the variable.