### Overview
- Pointers
- Top-down design with functions
- Selection structures (`switch` and `if`)
- Repetition and loops
- Logical operators
- Modular programming

### Pointers
- We create a pointer with `type *varname`. For example, `double *a`.
- We can get the address of a variable with `&varname`. 
	- We use this for pass by reference!
- Pointers store memory addresses. So you would do something like `a = &miles`.
- We can then update the value of `miles` through our pointer `a` with `*a = 10`
- When we pass a memory address into a function, the function is really using a pointer as the input variable. So `int scanf(double *ptr) {...}` gets defined, and so if I do `scanf(&miles)`, then we can see that we have `ptr = &miles`. 
	- Pass by reference.
- If you just pass a variable name, it's pass by value.

### Selection Structures
- I am *so* surprised that we're learning this. I have ***no*** clue what the syntax will be or how they will work.
- You know the syntax for this.

### Loops
- See the above. I'm so done with this.
- I just want to program, not look at syntax. Set me free.