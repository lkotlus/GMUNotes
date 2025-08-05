### Design Examples
- How do we actually go about implementing things with these?
- Well, we want to decompose problems into binary statements, possibly make a truth table, and then it's super easy!
- Regardless of complexity, there's three steps:
	1. Specify desired behavior
	2. Synthesize and implement
	3. Test and verify
- I mean, that's about it.
- Three-way light control:
	- We have a room with three doors, and a switch by each door controls a single light in the room.
	- Let $x,y,z$ denote the state of the switches.
	- Assume the light is off if all switches are open.
	- Closing any switch turns the light on.
		- Closing another switch will have to turn the light off.
	- Light is on if any one switch is closed and off if two (or no) switches are closed.
	- Light is on if all three switches are closed.
	- The below truth table clearly shows: $f(x,y,z)=\sum m(1,2,4,7)=\overline{x}\overline{y}z+\overline{x}y\overline{z}+x\overline{y}\overline{z}+xyz$

|$x$|$y$|$z$|$f$|
|-|-|-|-|
|0|0|0|0|
|0|0|1|1|
|0|1|0|1|
|0|1|1|0|
|1|0|0|1|
|1|0|1|0|
|1|1|0|0|
|1|1|1|1|

- Multiplexer Circuit:
	- It's often necessary to choose data from exactly one of a number of sources.
	- Design a circuit that has an output, $f$, that is exactly the same as one of two data inputs ($x,y$) based on the value of a control input, $s$.
		- If $s=0$, $f=x$. If $s=1$, $f=y$.
	- The function $f$ is really a function of three variables ($s,x,y$).
	- This gives $f(s,x,y)=\sum m(2,3,5,7)=\prod M(0,1,4,6)$.
	- Equal amounts of both, so I'll take SoP.
	- $f(s,x,y)=\overline{s}x\overline{y}+\overline{s}xy+s\overline{x}y+sxy$
	- We can very clearly simplify this: $f(s,x,y)=\overline{s}x+sy$.
	- Let's say we want to do PoS: $f(s,x,y)=(s+x+y)(s+x+\overline{y})(\overline{s}+x+\overline{y})(\overline{s}+\overline{x}+\overline{y})$.
	- This is less intuitive, but generally the same thing. $f(s,x,y)=(y+\overline{y})(s+x)(x+\overline{x})(\overline{s}+\overline{y})$
	- $f(s,x,y)=(s+x)(\overline{s}+\overline{y})$.

|$s$|$x$|$y$|$f$|
|-|-|-|-|
|0|0|0|0|
|0|0|1|0|
|0|1|0|1|
|0|1|1|1|
|1|0|0|0|
|1|0|1|1|
|1|1|0|0|
|1|1|1|1|

- Neat
- Car safety alarm:
	- Design a car safety alarm considering four inputs:
		- Door closed $D$
		- Key in $K$
		- Seat pressure $S$
		- Seat belt closed $B$
	- The alarm, $A$, should sound if:
		- The key is in and the door is not closed, or
		- The door is closed and the key is in and the driver is in the seat and the seat belt is not closed.
	- We can just read this off $A=\overline{D}K+DKS\overline{B}$
- Adder circuit:
	- So we need to take in two bits and output two bits.
	- For the sum bit, it's just XOR. For the carry bit, it's just an AND.
	- $S(x,y)=x\oplus y,\ C(x,y)=xy$
- Majority circuit:
	- Design a circuit with three inputs ($x,y,z$) whose output, $f$, is 1 if and only if a majority of the inputs are 1.
	- $f(x,y,z)=xyz+xy\overline{z}+x\overline{y}z+\overline{x}yz$.
	- Legit.