### State!
- Flip-flops are frequently used for this. We want to store a bit in a memory element. (we'll get to this on Thursday)
- Think of a car alarm. We want to set and reset the alarm based on a memory element. A sensor will set the alarm, and some sort of manual button will reset it.
- The most basic memory element is essentially just two inverters. We store a signal in between the two of them.
- We can also create a memory element with NOR gates.
- Basic SR latch:
	- Uses two NOR gates
	- Can basically store state fro two things.
	- $S$ and $R$ are used to handle $Q_a$ and $Q_b$.
	- $S$ and $R$ should never both be 1.

|$S$|$R$|$Q_a$|$Q_b$|
|-|-|-|-|
|0|0|0/1|0/1|
|0|1|0|1|
|1|0|1|0|
|1|1|0|0|

- When $S$ and $R$ are 0, we just have our state stored.
- We need to worry about propagation delay with this circuit to prevent collisions with $S$ and $R$.
- Gated $SR$ latch is pretty much the same as a normal $SR$ latch, but there's a switch that let's us control if the state can change.

|$Clk$|$S$|$R$|$Q(t+1)$|
|-|-|-|-|
|0|0|0|$Q(t)$|
|1|0|0|$Q(t)$|
|1|0|1|0|
|1|1|0|1|
|1|1|1|x|

- Essentially we have the same stuff going on with $S$ and $R$. $Q(t)$ is $Q$ at a particular time. If we enable $Clk$, we have essentially set off a burst (say from a push button) that allows us to updated the next value of $Q$.
- Our outputs of a gated $SR$ latch is $Q$ and $\overline{Q}$.
- The gated $SR$ latch can be implemented with all NAND gates.
- A gated $D$ latch uses a $Clk$ and $D$ (data). $D$ gets inverted going into the bottom NAND and goes directly into the top NAND to be $R$ and $S$ respectively. It uses all NAND gates.
- Level sensitivity:
	- If the output of a latch is controlled by the level of the clock input, the latch is level sensitive (this is all of the latches we've seen)
- It's possible to design a storage element where the output only changes at the point in time when the clock changes from one value to another:
	- This is called edge triggered.
	- Positive edge trigger:
		- Sensitive going from 0 to 1
	- Negative edge trigger:
		- Sensitive going from 1 to 0
- Propagation delays SUCK!
	- We need to hold a setup time for $D$ before the clock ($t_{su}$)
	- We need a hold time for $D$ to stay after the clock ($t_h$)
	- Typical CMOS values for these are $t_{su}=3\text{ ns}$ and $t_h=2\text{ ns}$. (nanoseconds)