### Transistors
- NMOS (n-type MOS) and PMOS (p-type MOS) are types of MOSFETs (Metal Oxide Semiconductor Field Effect Transistor)
- The difference between an NMOS and PMOS is just that $V_G$ has an inverter for the latter. 
- Between the two (NMOS and PMOS) we can eventually get CMOS (Complementary MOS).
- NMOS pulls drain to ground when turned on
- PMOS pulls drain up to $V_{DD}$ when turned on
- CMOS is used for several analog circuits such as sensors, data converters, and highly integrated transceivers for many types of communication
- CMOS has high noise immunity and low static power consumption. We don't have a lot of waste with CMOS.
- CMOS logic gates involve NMOS transistors in a pull-down network (PDN) and PMOS transistors in a pull-up network (PUN).
- The functions realized by the PDN and PUN are complements of one another ($\text{PDN}=\overline{\text{PUN}}$)
	- We need the same number of PDN and PUN as a result
- We can construct some neat logic gates out of these.
- Use sequence to make an AND condition to go to either $V_{DD}$ or $GND$, use parallel to make an OR condition to go to either $V_{DD}$ or $GND$.
- NOT just needs to transistors.
- AND and NOR both have implementations that require only 4 transistors!
- Logically, an AND/OR gate requires 6 transistors because we need to invert it with a NOT gate (+2 transistors)
- Transmission gates are really cheap, just two transistors!
	- Tri-state buffers need three inverters and a transmission gate, resulting in 8 transistors. Pricey!

### Flip-Flops, Registers, and Counters: Latches
- We can store information! We can have state!!!
- This is where it gets really cool.