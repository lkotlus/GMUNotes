### Syllabus and Introduction
- Professor Yun is an adjunct professor at GMU, he works at the FCC. He also does the "gauge how many CYSE majors there are" thing. Funny how that happens with these courses.
- We aren't going to do much analog stuff, only enough to explain how we get to digital. Analog signals are continuous, but digital is discrete (usually in bits, as well).
- We will define a system as something that has an input and output.
	- NOT the correct definition of system. A system is a collection of components that exhibit a behavior not seen within its individual parts.
- Weekly homework assignments posted and submitted on blackboard. Solutions can by typed, handwritten, scanned, photographed, etc. The only thing we need to do is put it all into one file. Homework is 25% of the grade.
- Exams are closed book, closed note, no devices. We have only one midterm (25%) and final (35%). If I do better on the final (cumulative exam), the final grade will be used for half of my midterm grade.
- Labs are 30% of the grade, gotta do well on the lab. 
- Class grade is curved to fit a B+ in the standard deviation. Insanely generous.
- The hardest part of this course will be understanding the problem solving approach. The math in the course is simple, but we are doing things very differently.
	- I feel like I should understand it decently well already, but those are famous last words.
- Lots of cool concepts approaching, I'm very excited.

## Lecture!
### Analog Signals
- Analog is a continuous signal.
- Time
	- Every time has a value associated with it, not just some times.
- Magnitude
	- A variable can take on any value within a range.
- Example:
	- Temperature, voltage, current, weight, length, brightness, color, etc.
- We can "digitize" an analog signal by picking certain evenly spaced points and converting them.

### Digital Signals
- Discontinuous
- Time
	- Discrete, sampled.
	- The variable is only defined at certain times.
- Magnitude 
	- Quantized
- Example:
	- Digital stuff

### Converting Analog to Digital
- To increase the quality of a digital signal, you approach analog by decreasing the change in time.
	- Think of a 1x1 image, a 4x4, and so on. You eventually approach what might as well be a continuous painted image because you have so many pixels.
- This slide looks like a Riemann Sum. 
- Quantization!
- **Quantization error** is a result of not getting enough samples.
- So we have a sensor, which goes into a sampler (stop/hold), which goes into an ADC (analog digital converter), which goes into a binary encoder, which finally arrives within our digital system. Lovely.
- Digital is great because we can compress things and keep high qualities.
- Digital is ubiquitous
	- Electronic circuits based on digital principles are widely used.
	- Microwaves, watches, phones, games, engine controllers, etc.

### VHDL
- VHSIC (Very High Speed Circuit) Hardware Description Language.
- A formal language for specifying the behavior of digital circuits.
- Only going over this for one class for like 30 minutes.

### Digital Hardware
- Logic circuits are used to build computer hardware as well as other digital hardware products.
- Late 1960s and 1970s saw a revolution in digital capability
	- Smaller transistors, larger chip sizes
- More transistors lead to more powerful circuits!
- Integrated circuits are fabricated on silicon wafers.
- Wafers are cut and packaged to form individual chips.
- Chips have from tens to millions of transistors now.
	- Quantum tunneling will stop us from going any smaller :(
