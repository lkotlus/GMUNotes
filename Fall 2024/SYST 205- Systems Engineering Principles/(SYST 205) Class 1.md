Professor is Mr. Icore. I got to know him for about five minutes before class. 

# Pre Lecture

### Classes
- No attendance
- If I don't motivate others to get group work done in class, I will end up doing it out of class.
- Motivate others, get more done. Makes sense.
- I like this guy, he's pretty legit.
- He works for the worlds largest electronic health record. Cool.
- "What does systems engineering have to do with CYSE? We will get to that." :)

### Work
- We will have lectures and then group work on applying concepts from it.
- We are here to make systems happen. In a lecture we will see the life cycle of a system and our place in it.
- We will not be graded on presentation skills, but it is a good opportunity to work on them.
- **Work hard to stay within the given amount of time/space**
- "If it is on page two, I will not read it and I will not grade it" (sources go on the second page, so that is allowed)
- We have one page for individual assignments. We have style guides. 
- There will be content that we cannot fit. We must choose what is most important to convince the TA and professor that we understand the material and content.
- We are not graded on grammar, but don't be terrible. Go through with a grammar check. Make sure you communicate what you mean.
- Write simply, concretely, and directly with purpose. Outline our answers to make sure that it is concise. "Think for a few minutes before you start answering."
- We will prepare PowerPoint slides for presentations. There will be strict time limits due to there being eight groups.
- We must rehearse for presentations to make sure it goes smoothly.
- Don't rush through things. Go at a normal speaking cadence and figure out how to fit the right amount of time. We must cover the key points of the presentation.
- A large group consists of two small groups. A small group stays together throughout the whole semester, but you will go with several other small groups as large groups.
- Assignments build upon one another, so the first assignment is scored more leniently due to having low context. Later ones are more strict.

### Class behavior
- He likes participation.
- Every exam is open notes, internet, brain. Open everything but another human being. Every question is an application question asking me to do something that we have done before.
- "If you do not come to the classes to see what we have done, your ability to do well on the exams will suffer."
- "The first seven pages of Google will have the wrong answer. Generative AI will have the wrong answer as well." (regarding exam questions)
- Groups are assigned randomly (oof).
- Exam is take home.

### General policies
- The last submission is the one that is graded.
- Late assignments discussed in lecture get a 0.
- Late assignments not discussed in lecture get this weird treatment, just do it on time.
- Accommodations must be made equitably to every student.
- FERPA! Must send all emails from my GMU account.
- If I get sexually assaulted (highly likely for people like me frfr) and tell Mr. Icore, he is obligated to report it.
- This guy is surprisingly liberal. Supports Diversity Equity and Inclusion stuff.

My work alarm went off right in the middle of class. Super loud alarm sound. So fun, loved that.

### Resources
- The university provides something called magic draw.
- It is a systems engineering thingy, but we don't need to use it.
- PowerPoint, MS draw, etc. are just fine.

### TA and office hours
- TA is Ms. Jeng Chu-ehuan (Julia).
- Office hours for her are 9 AM - 10 AM via zoom. In person by appointment.
- Office hours for Mr. Icore are by appointment only.

### Epic tip
- The is a rubric on assignments!
- Read the rubric first and make the assignment easy to grade.
- Easy to grade --> higher grade.
- "If I need to look for the answer, I assume it is not there."
- Make it easy to find. Outline it and make it easy for him so that you get an easy grade. Lovely stuff.

### Group stuff
- Randomly assigned, but if someone didn't participate they get a zero.
- "Let group members know this if they were not here."
- We will be providing detailed reports on our group-mates and what they got done.
- Personal vendettas are clear to see for the professor because he can see that only two people are pointing at each other, but others just tell the truth.

# Actual Lecture!

### Semester group
- Making a universal ubikey thing

### Key terms
- A **system** is a collection of components.
- An **engineered system** is an open system of technical or sociotechnical elements that exhibits emergent properties not exhibited by its individual elements. 
	- A mechanical watch is made of gears and springs with a face and hands and some paint, it tells time. These components do not do things individually that the whole can do. Here, telling time is the emergent property.
	- These systems serve different purposes from different perspectives. For me, my laptop is a tool. For Dell, it is a product.
	- It has a life cycle and evolution dynamics.
	- A system must account for a boundary and an environment that it operates within.
	- The system is most likely part of system-of-interest hierarchy (either a personal preference or one of different systems)
- A **system of systems** is every day system that can be construed as being part of a larger, enclosing system. 
	- You can have a discrete number of systems that come together in a federation (in the same way an engineered system does), exhibiting behaviors beyond the scope of an individual system.
- **Systems engineering** is "an interdisciplinary approach and means to enable the realization of successful systems" (INCOSE 2015).
	- You need a ton of different engineers that do all sorts of different things. Systems engineering reaches everything from STEM and beyond.
- A **systems engineer** is just a person who practices systems engineering as defined above. Their engineering skills/experience include sustained practice, specialization, leadership, or authority over SE activities. "Visionaries of the system".

### Introduction to systems engineering
- Consider a railway system (London to Glasgow)
- It must achieve a journey time from London to Glasgow in less than 250 minutes.
- Well, what does this requirement mean? What are the implications?
	- Well, what about stops along the way? We are definitely not going to be able to say "well, it takes X miles and 250 minutes gives this average speed."
- This single requirement must be fulfilled through coordination of each and every major component within the system:
	- Trains (speed)
	- Tracks (support of high-speed trains)
	- Stations/staff (waiting time caused by them)
	- Drivers (controlling the trains)
	- Signaling subsystems (be efficient with the trains)
	- Train control and detection subsystems (report data quickly and correctly)
	- Power delivery subsystems (don't bottleneck the trains)
- The best solution will involve the whole system, not select components.
- **Systems engineering doesn't necessarily give the best answer, but it does explain why the easy answer that everybody knows is wrong.**

#### Simple system: a cup
- It has components!
	- A handle
	- Cylindrical (parabolic, hyperbolic, doesn't matter) container
- A handle cannot help you drink. A container can, but it sucks for hot drinks, because you burn yourself! The two components together we get an emergent behavior of a cup you can use to drink hot liquids without burning your hands.
- So what is our purpose?
	- Allow someone to ingest hot or cold liquid without something horrible happening to them.
- Requirements:
	- Place on a flat surface
	- Can be held
	- Can be filled with fluid and be emptied
	- Hold the liquid sustainably
	- Deliver fluid to a human mouth (because it's a cup)

### Key elements of systems engineering
- A system does not simply appear. No spontaneous generation.
- There are a set of processes that let us move from idea to a series of steps allowing us to physically manifest the system.
- A system is sustained throughout the entire life cycle, so this lasts (by definition) longer than the actual usage.
- Taking stakeholders and demands figuring them out, getting optimal parameters, and setting up restrictions and requirements from that.
- The systems engineer must analyze, specify, design, and verify the system is functional and fulfills all requirements.
- We care about systems engineering in cyber security because we need to balance a ton of people all fighting for opposing goals (it should be easy to access vs. it should be secure), and we must optimize the result to make it the best possible system.

### A systems development life cycle (not all required)
- Initiation
- System Concept Development
- Planning
- Requirements Analysis
- Design
- Development
- Integration and Tests
- Implementation
- Operation and Maintenance
- Disposition

### Systems and Systems Engineering
- A system may be an engineered, natural, or social system. Potentially all three.
- **Natural Systems** are those that occur naturally (genius)
- **Social Systems** are systems created by people interacting
- **Engineered Systems** (seen above as well) are designed by someone through use of knowledge through several different branches of science and engineering.

### Concept definition
- Concept definition is the set of SE activities where the problem space and needs of stakeholders are closely examined. This begins before a formal definition of the system.
- Don't go straight to solving the problem. **Understand the problem and the stakeholders first.**
- What and why must be tackled first as questions. How is a development question, but we need to know what the reasons are for the system as well as what the system actually is.
- **Mission analysis** is figuring out what the problem is, who the stakeholders are, who gets a vote, identify operation concepts (how at a big cartoon level will this work?), and distinguish environments and constraints that bound our solution space.