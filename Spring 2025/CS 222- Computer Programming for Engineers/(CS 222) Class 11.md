### Strings
- `strcmp()` returns 0 when the strings match, which is weird.
- `strlen()` doesn't include `\0` in the length, which is also weird.
- Frequent functions:
	- `%s` for strings in `printf()` and `scanf()`
	- `strlen()` (gets length, ignoring the terminating `\0`)
	- `strcpy()` (copies a string)
		- `strncpy()` (copies n characters of a string)
	- `strcmp()` (compares strings, returns 0 for match)
		- `strncmp()` (compare first n characters of strings)
	- `strcat()` (concatenates strings)
		- `strncat()` (concatenates the first n characters a string)
	- `strtok()` (Separate a string into tokens by its delimiters, like split)
- Today we're doing `sprintf()` and `sscanf()`, which are included in `stdio.h`.
- `sprintf()`
	- Instead of printing to `stdout`, we are going to store in a string.
	- `sprintf(str, "...", ...);`
	- Pretty simple.
- `sscanf()`
	- Instead of scanning from `stdin`, we are going to scan a string.
	- `sscanf(str, "...", ...);`
	- Also simple.
- Some character related functions (from `ctype.h`):
	- `isalpha()` (`[a-zA-Z]`)
	- `isdigit()` (`[0-9]`)
	- `islower()` (`[a-z]`)
	- `isupper()` (`[A-Z]`)
	- `ispunct()` (`[[:punct:]]`)
	- `isspace()` (`[[:space:]]`)
	- `tolower()` (Switches from upper to lower)
	- `toupper()` (Switches from lower to upper)
- `getchar()`:
	- Gets one character from `stdin`. That's the whole thing.
- We can't return arrays (string or otherwise) from functions because all memory in the function is deallocated when it stops running. Must do pass by reference.

### Structs
- It's over. I know structs now.
- We want to make our own data types. We want them to be amazing and epic.
- But there's no objects, so how do we do it? We do it with structs.
- Imagine if objects didn't have inheritance or methods or anything like that. Just data types.
- We use dot notation.
```c
typedef struct {
	char name [STRSIZ];
	double diameter;
	int moons;
	double orbit_time, rotation_time;
} planet_t;
```
- With the above struct, `planet_t`, we can create a new variable with that type! That would be `planet_t earth;`. Really cool!
- Furthermore, we can set and read values with the aforementioned dot notation. That looks like `earth.diameter = 1000;`, `printf("%lf\n", earth.diameter);`.
- We can also pass individual parts of structs into functions. `strcpy(earth.name, "Earth");`
- Files can be stored with `FILE *varname = fopen(...);`. This is neat. We can then read from the file with `fscanf()`.