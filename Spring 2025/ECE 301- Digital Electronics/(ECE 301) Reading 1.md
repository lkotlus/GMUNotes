# Reading: Chapter 1

## Introduction
- In this course we are studying logic circuits.
- We will learn how to derive them from simpler ones, describe them with Verilog, and display them with CAD.
- So cool!

### 1.1 - Digital Hardware
- Digital hardware is any product with a logic circuit.
- We've gone from individual transistors to silicon wafers as integrated circuits. Microprocessors are now made from single chips.
- Moore's law predicts how many transistors we can fit onto a single chip. It should hold true for several more years.
- The International Technology Roadmap for Semiconductors (ITRS) tracks and predicts process in computing hardware.
- Chips can be placed together on Printed Circuit Boards (PCBs)
- Three types of chips are used for designing circuits:
	- Standard Chips
	- Programmable Logic Devices
	- Custom-Designed Chips
#### 1.1.1 Standard Chips
- Single function, using around 100 transistors or less.
- Standard functions that are frequently used.
- Take up more space on the PCB than is worth, but was popular in the 1980s. 
- Functionality of each chip is fixed, and cannot be changed.
#### 1.1.2 Programmable Logic Devices
- The opposite of a standard chip, PLDs can be changed to fit the needs of the user.
- This is done via programmable switches that are configured by the end user.
- These chips have a very general structure, but the most commonly-used PLD is a Field-Programmable Gate Array (FPGA).
- The largest FPGAs contain billions of transistors, and support implementation of complex digital systems.
- FPGAs are widely used today.
#### 1.1.3 Custom-Designed Chips
- FPGAs are not optimized for the task you program them for, and they frequently take up more space than they need. 
- In some cases, it is possible to design a chip, send the design to a manufacturer, and have it sent to you. 
- This approach is called custom, or semi-custom design.
- Such chips are sometimes called Application-Specific Integrated Circuits (ASICs)
- These cost more to manufacture, but increased performance helps with quality. Furthermore, if you sell a lot of the product, it costs less to manufacture in bulk. Finally, because you take up less space on the PCB, size goes down, and manufacturing costs go down as well.
- The other major drawback is time. It can take months to design a chip.

### 1.2 - The Design Process
- SDLCs and whatnot.

### 1.3 - Structure of a Computer
- A computer is a grouping of PCBs, all of which have many chips.
- This course will focus on the design of logic circuits on those chips.
- We will also discuss transistors and how they work.

### 1.4 Logic Circuit Design in this Book
- Verilog and CAD.
- Well suited for development on FPGA chips.

### 1.5 Digital Representation of Information
- Binary! If you have current, 1, if you have no current, 0.
- Digital is discrete, analog is continuous.
#### 1.5.1 Binary Numbers
- Binary to decimal conversion, how exciting!
- We call the right-most bit the least-significant bit (LSB) and the left-most bit the most-significant bit (MSB).
#### 1.5.2 Conversion Between Decimal and Binary Systems
- You know this.
#### 1.5.3 ASCII Character Code
- Each letter/symbol is a number.
- American Standard Code for Infomration Interchange
#### 1.5.4 Digital and Analog Information
- Convert with a digital-to-analog (D/A) converter.

### 1.6 - Theory and Practice
- Modern design uses CAD, but this didn't always exist.
- A great deal of "theory" has been created on properly designing these incredibly complex circuits.
- CAD makes it possible to design complex circuits, but it also helps make them simpler by doing the theory for us.
- Why learn the theory, then?
- Three big reasons!
	- The designer must describe the final circuit
	- The algebraic rules are required to design better CAD tools
	- You need to choose the correct steps for CAD to take
	- Bonus: it's interesting and intellectually challenging