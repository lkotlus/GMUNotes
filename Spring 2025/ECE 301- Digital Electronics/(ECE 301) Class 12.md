### Three Level Synthesis
- So normally we get everything in two levels. SOP is AND and then OR. POS is OR and then AND. NAND is NAND and NAND, NOR is NOR and NOR. 
- In order to get to three levels, we need to manipulate the Boolean expression: $$AB\overline{C}+B\overline{C}D+A\overline{B}C$$ $$(A+D)B\overline{C}+A\overline{B}C$$
- We can do this in three levels, and we can even convert this to NAND-NAND if we want. Replacing $(A+D)$ with NAND require's DeMorgan's law: $$(A+D)$$ $$\overline{\overline{(A+D)}}$$ $$\overline{\overline{A}\cdot\overline{D}}$$
- We can get 3-level NOR with POS as well: $$(A+\overline{B})(\overline{A}+D)(\overline{A}+B+C)$$ $$(A+\overline{B})(\overline{A}+(D)(B+C))$$ $$(A+\overline{B})(\overline{A}+DB+DC)$$
- This gives us 3-level POS, which can also be turned into NOR-NOR. The DeMorgan's for our $DB$ and $DC$ terms can be seen below: $$DB$$ $$\overline{\overline{DB}}$$ $$\overline{\overline{D}+\overline{B}}$$
- For real for real.

### Number Representation and Arithmetic Circuits
- Mainly unsigned addition.
- So the decimal system works like this: $$(abcd)_{10}=10^3a+10^2b+10c+d$$
- We are represented by $n$ decimal digits: $D=d_{n-1}, d_{n-2}, ..., d_0$
- This is just: $$\text{V}(D)=d_{n-1}10^{n-1}+d_{n-2}10^{n-2}+...+d_110^1+d_010^0$$
- We can switch to binary with $n$ digits: $B=b_{n-1}, b_{n-2}, ..., b_0$: $$\text{V}(B)=b_{n-1}2^{n-1}+...+b_02^0$$
- We can do DTB conversion with the good old repeated division strategy. LSB is top, MSB is bottom.
	- Repeated multiplication for fractional components! MSB is top, LSB is bottom.
- To generalize what we have, for any base number system given a radix $r$ and digits $K$: $$\text{V}(K)=\sum_{i=0}^{n-1}k_{i}r^i$$
- That doesn't really work for fractional components, if you have them, initialize $i$ to the negative number of fractional digits we have. So for 4 fractional digits: $$\text{V}(K)=\sum_{i=-4}^{n-1}k_{i}r^i$$
- With this recap out of the way, let's talk about binary addition. It's really just a bunch of XOR gates, and you can get your carry bit with an AND gate.
- Binary subtraction is kind of identical given a borrow bit and removing the concept of the carry bit.
- We will implement full circuits on Thursday!