### Midterm Thursday (Class 14)
- Things we will see:
	1. Evaluation rules/operator precedence 
	2. Input validation (loop)
	3. User defined functions and input/output parameters
		-  Function declaration/prototype, call, and definition (including arrays)
	4. Visualizing pointers in memory
	5. Strings (`sprintf` and `scanf`)
	6. Sentinel controlled loops
- You should write a program that does a bunch of string stuff. That will help you to learn all of the functions.
	- Do the date string example from class!

### Structures!
- I love structures. 
- Notes on strings:
	- If you define a character array, you *must* terminate it with a null character to terminate the string!
- He took all my class time doing a silly coding example for strings. And I mean coding, not programming. Code. Gross.
- So let's say we have a struct `a` and a pointer to it, `struct_ptr`.
	- `*struct_ptr.thing` is compiled as `*(struct_ptr.thing)`.
	- `(*struct_ptr).thing` is what we're trying to do.
	- The shortcut for this is `struct_ptr->thing`. I don't like it, and don't plan on using it.
- 