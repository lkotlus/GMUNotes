### Review From Last Class
- I love this so much, it's the best. Who even wants memory safe languages?
- Sort of like class 1 part 2. Homeboy keeps asking me to look at the guides for UNIX and vim. UNIX and vim are my entire life.
- Review from last class:
	- CPU runs operation and manages memory.
	- Our different data types have different sizes.
		- A `char` is 1 byte, or 8 bits. This gives us 256 potential values for characters.
		- `int` is 4 bytes, or 32 bits. That's $2^{32}$ values, or 4,294,967,296.
	- We compile our programs with `gcc`.
	- SCRAT - Save, Compile, Run, and Test
		- Maybe if I wasn't the greatest programmer to ever live.
		- (this is good advice)
	- Decimal to binary to hex:
		- If someone teaches this to me one more time I am going to swan dive off a building.
	- Data in CS is discrete:
		- We can count everything.
		- Signed and unsigned shenanigans.

### UNIX
- Operating system! It's software than:
	- Manages the resources of the computer (CPU, memory, devices, etc.)
	- Provides programmers and users with an interface to access those resources.
- Shell: user interface based on a command-line interpreter
	- Windows provides a secure shell
		- Putty, Bitvise, and even PowerShell now
	- MacOS provides a secure shell
		- Cyberduck
	- Linux
		- The OG: `ssh`
		- For the actual shell, we're using bash.
- UNIX commands!
	- We have commands, which use system calls to do things!
	- Let's see if there's a single command on this slide that I don't recognize:
		- `du`: "disk usage", estimates file space recursively for a directory
		- `wc`: "word count", print newline, word, and byte counts for a file
		- `less`: you can go through a file without loading the whole thing, pretty useful for me actually.
		- `script <filename>`: creates a bash script from your actions, super cool
	- `|`, `||`, `&&`, `>`, `<`
		- I LOVE BASH ONE-LINERS
	- Professor keeps talking about how he uses these things "in industry", I love it.
	- `~` is home directory (you know this), but `~<username>` takes you to that user's home directory. Neat!

### Vi/Vim
- Command, insert, visual.
- So epic, so home row.

### IO redirection from/to files
- `>`, `>>`, `<`

### Introduction to C
- C is the programming language that was used to implement UNIX.
- We are a low-level language, we have DIRECT access to memory and need to manage it ourselves.
	- A lot of languages were developed in C
	- Lots of low-level scripts are C-like programming components
- Static types!
	- Type casting with the same syntax as Java: 
	```C
	int a = 1;
	float b = (float)a;
	```
	- Pretty cool.

### Programming Assignment 1
- Calculate the percentage of free disk space remaining.
- So boring, we don't even get the values through system calls. We need to ask the user and `TOTAL_DISK_SPACE` as a constant. Gross.