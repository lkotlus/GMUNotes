### MUX
- Okay so we want to derive the circuit $f=\overline{w}_2\overline{w}_3+w_1+2_2$ as a single 2-1 MUX.

|$w_1$|$w_2$|$w_3$|$f$|
|-|-|-|-|
|0|0|0|0|
|0|0|1|0|
|0|1|0|0|
|0|1|1|1|
|1|0|0|0|
|1|0|1|1|
|1|1|0|1|
|1|1|1|1|

- We can see from this that we just have:

|$w_1$|$f$|
|-|-|
|0|$\overline{w}_2\overline{w}_3$|
|1|$w_2+w_3$|

- Shannon's Expansion Theorem
	- Any Boolean function can be written in the form: $$f(w_1,...,w_n)=\overline{w}_1f(0,...,w_n)+w_1f(1,...,w_n)$$
	- This expansion can be done with any of the $n$ variables.
	- We use the chosen variable as the select input for the MUX, and our outputs are $f(0,...,w_n)$ when $w_1=0$ and $f(1,...,w_n)$ when $w_1=1$.
- For the function $f(w_1,w_2,w_3)=\sum m(0,2,3,6)$, use Shannon's expansion to derive an implementation using a single 2-1 MUX:
	- Alright, so we have $f=\overline{w}_1\overline{w}_2\overline{w}_3+\overline{w}_1w_2\overline{w}_3+\overline{w}_1w_2w_3+w_1w_2\overline{w}_3$
	- Expansion of $w_1$ allows us to realize: $$\overline{w}_1(\overline{w}_2\overline{w}_3+w_2\overline{w}_3+w_2w_3)+w_1(w_2\overline{w}_3)$$
	- Simplifying further shows us that: $$f(w_1,w_2,w_3)=\overline{w}_1(w_2+w_3)+w_1(\overline{w}_3)$$ 

### Decoders, Demultiplexers, Ecoders, and Code Converters
- Decoder circuits decode encoded information
- Binary decoder has $n$ data inputs and $2^n$ outputs
- Only one output is asserted at any time and each output corresponds to one valuation of the inputs
- An Enable Input ($En$) is used to disable the outputs
	- If $En=0$, none of the decoder outputs is asserted
	- If $En=1$, one of the outputs is asserted according to the valuation of the inputs
- Decoders and multiplexers are very similar.
- Demultiplexers are just the opposite of multiplexers
- Encoders are the opposite of decoders. $2^n$ inputs to $n$ outputs.

### Standard Chips
- I mean, just like the labs. Read schematics.
- Most of these are implemented with Diode-Resistor Logic (DRL).
- 7400 series chips are cool, we use them in labs.
- PLDs are very popular as they are general purpose.
- PLAs (Programmable Logic Arrays) are epic
- PAL is just like PLA, but the OR plane is fixed. We will focus on these.
- Most actual PAL devices include extra circuitry at the output of each OR gate to provide additional functionality.
- The term macrocell refers to the OR gate combined with the extra circuitry.