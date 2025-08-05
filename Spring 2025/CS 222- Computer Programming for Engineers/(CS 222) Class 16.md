### Finishing Modular Programming
- Header files and whatnot
- Header files are just pre-processor directives, structs/unions, and function declarations. That's the whole thing.
- `gcc -c [C_FILENAME]` to get our object file, `gcc -o [OUTPUT_EXE] [OBJECT_1] ... [OBJECT_N]` to link our object files.
- The `make` command will automatically use any file named `Makefile` or `makefile`. If you want to name it something else like `project_makefile` or `linked_list.makefile`, you need to do `make -f [FILENAME]`.
- `make clean` will usually just get rid of all created files.
- `$@` is the current file, `$<` is all of its dependencies, and there's some other stuff we can do.
- `make -k` compiles everything even if you get an error somewhere else.

### Programming Assignment 3
- Turn firewall logs into an array of structs.
- I mean, it's super easy. Docker for extra credit, which is neat.
- We're going to need to use `gdb` in the script file. We'll discuss that more later, but it's pretty easy.

### `gdb`
- RTFM. It's so easy, just set breakpoints and do debugging stuff.