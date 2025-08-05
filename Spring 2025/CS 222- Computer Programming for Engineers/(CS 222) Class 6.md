### Loops
- These exist.
- While loops loop while something is true.
```c
int num;
int input_status;

printf("Please enter a number: \n");
input_status = scanf("%d\n", &num);

while (input_status < 1) {
	printf("Please enter a number: \n");
	input_status = scanf("%d\n", &num);
}
```
- Do-while loops just check the condition *after* running the body. Note that when doing input validation it's a more elegant solution.
```c
int num;
int input_status;

do {
	printf("Please enter a number: \n");
	input_status = scanf("%d\n", &num);
} while (inputs < 1) // Basically the only use case for do-while.
```
- For loops are the best.
```c
for (int i = 0; i < n; i++) {
	printf("%d\n", i);
}
```
- You can use `break` to stop the loop prematurely. You can also use `continue` to just keep going. This is not best practice, just make things that work normally.
- Booleans do not exist in c. Don't as me why. Boolean expressions return a 1 or a 0, which makes sense I suppose.


### Functions
- I must become a functional boy.
- We need to define our functions before `main()`, so how do we do that?
- We can do it with function prototypes:

```c
/*
    Multiline comment
 */

#include <stdio.h>

int my_function();

int main() {
    function_prototype(2);
}

int my_function(int n) {
    printf("%d\n", n);
}
```

- We have that prototype at the top, which let's us call the function in `main()` without needing to write it fully top-down.
- Next time we will actually get to learn things.