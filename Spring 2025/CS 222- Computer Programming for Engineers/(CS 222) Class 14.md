### Structs, Continued
- Leading `0x` denotes a hex value, leading `0` denotes an octal value. For example: `int y = 0x77, x=077`. In this example, `y` is hex and `x` is octal.
- `strchr()` returns a pointer to the first character occurrence in a string. Neat.
- Text files are opened with `"r"` and `"w"`. For binary files, we just do `"rb"` and `"wb"`.

### Unions
- Unions are similar to structs, but only one member can contain a value at a time.
- This is useful because it allows us to essentially have a dynamically typed array or member of a struct.
- The size of a union is the largest of its members, unlike a struct which is the sum of its members.