### Outline
- Intro to C
	- `gcc`
- C language components
	- `#` preprocess directives
	- Data types
	- Function calling
- PA 1
- Operators and evaluation rules

### Intro to C
- `scanf()` returns an integer corresponding to the number of inputs provided.
- Division
	- `int/int` --> `int`
	- `int/float`, `float/int`, `float/float` --> `float`
- C process:
	- We start with our source code, get an object file (`*.o`), which can then be compiled to an executable. We skip the object file with the `-o` tag. Object files are important, as they can be linked.
	- C libraries are linked to executables.
- Basic tools:
	- `gcc` to compile (linking included)
		- `-g` to allow debugging
	- `gdb` debug
		- Discussed later in the semester
	- `make` project development tool for large programs with multiple files
		- Discussed later in the semester
- IDEs
	- Integrated Development Environments are very powerful.
	- Vim is better.
- Constants:
	- `const` creates an immutable value in memory.
	- `#define` basically just does a search and replace during the compiling.

|Data Type|`printf()`|`sizeof()`|
|----------|------------|-----------|
|`char`|`%c`|1 Byte|
|`int`|`%d`|4 Bytes|
|`float`|`%f`|4 Bytes|
|`double`|`%lf`|8 Bytes|

### C Language Components
- Single pass compiler, so we need to write our code top-down.
- Reserved words are a thing.