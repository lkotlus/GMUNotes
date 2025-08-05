### Recall...
- Structs are epic
- Unions only have one meaningful entity at a time
- Unions are the size of their largest potential entity
- Arrays of structs, arrays of unions

### Command Line Arguments and Makefiles
- Our main functions are going to look a little different to support command line arguments:

```c
int main(int argc, char* argv[]) {
	...
}
```

- So we have an `int` that stores the number of arguments we got (`argc`) and an array of character pointers to store each individual command line argument (`argv`).
- Completely random, but you can terminate the program from anywhere by using `exit(EXIT_CODE)`. In `main()` you would typically do this with a `return`, but if you return prematurely from a user-defined function, then nothing really happens.
- We count program name in the length of `argv`, so for something like `./addition 1 2`, we have `argc == 3`.
- Some useful functions:
	- `isalpha()`
	- `isdigit()`
	- ... Just think of any kind of character, put "is" before the name and that's what it does.
	- Just use regular expressions for anything large.
- Something cool:

```c
#include <stdio.h>
#include <stdlib.h>

int main(int argc, char* argv[]) {
	if (argc < 2) {
		fprintf(stderr, "ERROR: expected usage is %s FILE_PATH\n", argv[0]);
		return EXIT_FAILURE;
	}
	
	return EXIT_SUCCESS;
}
```

- So we can write to the `stderr` variable, and with that we can show error messages when returning an `EXIT_FAILURE`. 
- Finally getting to makefiles. We want to divide programs into components, and then use a makefile to put them all together.
- Header files
	- These store all the structs, function declarations/prototypes, and global variables.
	- Very useful, and works for compilation before linking.
- `make` is a utility for automatically compiling source code files into object files and linking object files into executables. Basic compilation manager, often used for C but is language agnostic.
- Makefiles are just scripts that define rules for compilations and linking by the `make` utility.
- Essentially, you create a makefile and run `make` on that makefile.
- Makefile format:
	- Makefiles are made up of rules. Each rule has a dependency and an action. 
	- Each rule is two lines:
```makefile
sum: main.o sum.o              # Dependency line
	gcc -o sum main.o sum.o    # Action line

main.o: main.c sum.h
	gcc -c main.c

sum.o: sum.c sum.h
	gcc -c sum.c
```
- Directed Acyclic Graphs (DAGs) are used to track dependencies of files. Each node is the parent of its dependencies. Acyclic because if we have cycles in our dependencies we are in big trouble. Sometimes called a dependency tree.
- We can create a DAG from this to show all the dependencies. We can also see how this works. 
	- We want to make a sum executable, and so we need to compile that by linking `main.o` and `sum.o`.
	- To get `main.o`, we need to compile `main.c`.
	- To get `sum.o`, we need to compile `sum.c`.
- Note that we need to work in sort of reverse order for this. We're recursing through our dependencies. 
- In order to optimize compile times, `make` uses last modified times to avoid compiling things that are unnecessary in the DAG.
- We can have multiple action lines. This is especially normal for something like a `clean` rule, which is for cleaning stuff up:

```makefile
sum: main.o sum.o              # Dependency line
	gcc -o sum main.o sum.o    # Action line

main.o: main.c sum.h
	gcc -c main.c

sum.o: sum.c sum.h
	gcc -c sum.c

clean:
	rm *.o sum
	ls -FC
```

- So we can see that if you use `make clean`, it will remove all object files as well as the final executable file. After that, it will show the contents of the project directory.
- Header files! If you're including a header file in the same directory, don't use `<>` like we have been. If it's in the same directory, use quotes. So:

```c
#include <stdio.h>
#include "gaming.h"
```

- `stdio.h` is not in the same directory, but `gaming.h` is.