### LUT (Lookup Tables)
- LUTs are lookup tables, and they can be implemented with several MUXs.

### Buffers
- In circuits where a logic gate has to drive a large capacitive load, buffers are often used to improve performance of circuits.
- Essentially it just amplifies the value.
- A tri-state buffer essentially is just a buffer with a switch.
- There's four types of tri-state buffers:
	- Inverting and non-inverting outputs
	- Active high and active low enable signals
	- In total we get:
		1. Inverting active high
		2. Non-inverting active high
		3. Inverting active low
		4. Non-inverting active low
- We can design MUX circuits with tri-state buffers
- Transmission gates are essentially just switches:

|$s$|$f$|
|-|-|
|0|$Z$|
|1|$x$|

- These are implemented with just two transistors and are commonly used to implement XOR gates and multiplexer circuits.
- 1 is a high voltage, 0 is a low voltage (negative), $Z$ is literally no voltage at all.