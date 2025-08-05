### This is really just notes for the final.
- So the multiple choice part did not go very well at all.
- I would go so far as to say that the entire thing was BS. He just put random crap on it that is useful to absolutely nobody. Least important information that I could ever think of. Cope.

### Background information
Consider a simple mathematical system consisting solely of integers with the following properties: Even, Odd, Positive, Negative; and in which only the following 7 transformations are allowed:

- +1 (increase integer by one unit)
- -1 (decrease integer by one unit)
- \*0 (multiply integer by zero)
- \*2 (multiply integer by two)
- /2 (divide integer by two, result must be an integer or the operation is not allowed in the system)
- \*1 (multiply the integer by positive one)
- \*(-1) (multiply the integer by negative one)

The following logical functions are defined in the system and return a True or False Result:

- \> or GT – greater than, X GT Y is true if X is a larger integer than Y, that is X minus Y is greater than 0
- < or LT – less than, X LT Y is true if X is a smaller integer than Y, that is X minus Y is less than 0
- == or EQ – equal to, X EQ Y is true if X is the same integer as Y, that is X minus Y is equal to 0
- (mod 2) –Modulo 2 arithmetic operation but only as a test, not a valid integer transformation, X (mod 2) is true if X (mod 2) = 0 otherwise it is false
- AND – A AND B is true if both A is true and also B is true
- OR – A OR B is true if at least one (or both) of A and B is true
- XOR – A XOR B is true if ONLY ONE of A and B is true
- NOT – NOT A is true if A is false

Examples: ((7 GT 10) EQ FALSE is a TRUE statement; (((10 < 12) OR (10 < 8)) AND (7 (mod 2))) is a FALSE statement; (NOT (15 (mod 2))) is a TRUE statement.

Parenthetical groupings are allowed to direct order of operations as per normal algebraic practice.

This system always starts at 0 (zero). For purposes of this system, Zero is neither even nor odd and neither is it positive or negative; however, Zero can be divided by two and the result is Zero. In this system, there are no such things as “prime” or “composite” numbers as these concepts overlap with even/odd.

### Part 1
**Consider that this system has 5 (five) states. Based only on the information and system definition provided in this question, identify the 5 system states. Explain why your states are correct in the context of the system definition.**

**15% - Each correctly identified state**
**5% - rationale for why each identified state is correct**

#### Part 1 Answer
Our states are:

1. Positive Even (PE)
2. Positive Odd (PO)
3. Negative Even (NE)
4. Negative Odd (NO)
5. Zero (Z)

Justification:

1. Integers can be even or odd as well as positive or negative. Because even/odd is independent of positive/negative, each (nonzero) integer will have one attribute from each grouping. From this, we will have a state for each permutation of the attributes. So, because a nonzero integer can be even/odd as well as positive/negative, a valid state is even and positive.
2. See the reasoning above. Because a nonzero integer can be even/odd as well as positive/negative, a valid state is even and negative.
3. See the reasoning above. Because a nonzero integer can be even/odd as well as positive/negative, a valid state is odd and positive.
4. See the reasoning above. Because a nonzero integer can be even/odd as well as positive/negative, a valid state is odd and negative.
5. Zero is the exception to the attributes that all other integers have within this system. We have defined it as non-negative, non-positive, non-even, and non-odd. This is a set of attributes unique to zero, therefore it is a state of its own.

### Part 2
**Consider that in the above system, we arbitrarily select an integer X at time T without knowing anything about its state or the transformations applied. Create an activity diagram that takes X from the system and FULLY categorizes it based on the collection of states available in this system.**  

**HINT: your activity diagram can start with “Select Random Integer X” so you can focus on the core activities of classification. You may only use the available operations defined in the system in your activity diagram.**

**15% Each potential state and the activity path to that state correctly represented in the activity diagram** 
**25% Activity diagram complies with visual grammar**

#### Part 2 Answer
![[DetermineState.jpg]]

### Part 3
**In the above system, in the context of Functional Diagram (IDEF-0), identify in detail, the following items in the context of the A-0 diagram level where the main function is “execute transformation” from the perspective of the person using this math system. Explain your choices. You do not need to draw the diagram, you need to identify the contents of each label and explain your decisions.  
a.    Inputs  
b.    Outputs  
c.    Controls  
d.    Mechanisms.**

**20% - Correct identification of the complete set of each of Inputs, Outputs, Controls, and Mechanisms based on the system definition**
**5% - rationale for why the identified set of each of Input, Output, Control, and Mechanism is complete and correct**

#### Part 3 Answer
1. Inputs  
    1. n  
        - The integer that the transformation is being performed on. Required for us to have the function "execute transformation" on something.  
    2. Writing materials  
        - Assuming the user writes down some of the input, output, and side work, writing materials are consumed throughout the function.  
    3. Transformation choice  
        - While the transformations themselves are a mechanism of the function, the selection of the transformation is an input of the user.  
2. Controls  
    1. Transformation restriction  
        - We cannot perform the /2 operation if n is odd, as that would output a number that is no longer an integer.  
    2. Math knowledge  
        - The user relies on their ability to perform basic arithmetic in order to properly use the system. If they lack knowledge of how to use an operation, they are essentially unable to use it. This is similar to the math skills mechanism, but there is a clear distinction with this being presence of knowledge, and that being the mental process of working out the problem.  
3. Outputs  
    1. n  
        - The new value of n after the transformation has been executed.  
1. Mechanisms  
    1. Math skills  
        - The person using the system must use their known math skills to work out basic arithmetic.  
    2. Writing tools  
        - The person using the system will most likely have a pen/pencil with paper, a dry-erase board, etc. to use with the system.  
    3. Transformations  
        - Although it is easy to label the transformation as an input, it is not consumed throughout the function. The transformation better fits the description of a mechanism, seeing as it is used to convert the input to output.

### Part 4
**Create a state diagram showing the interactions of the 5 states using the 7 allowed transformations. Ensure state transitions are correctly and completely defined. (state diagram correctly drawn). You must use the available operations within the system to define state transitions.**

**25% State Transitions correctly move from state to state**
**25% State Transitions correctly defined/labeled in diagram** 
**25% State diagram complies with visual grammar**
**25% All states and all transitions in diagram**

#### Part 4 Answer
![[States.jpg]]

### Part 5
**Assume the activity diagram context not shown is correct and you are given the below snippet of an activity diagram. What, if anything, is wrong with the following section of the below activity diagram? Explain and justify your answer.**
![[Picture1.jpg]]

#### Part 5 Answer
It uses a join after a decision even though joins are only used after forks. I would say that it does not account for the case of "x==0", but diagram context not shown is assumed to be correct, so if x can be equal to 0, there is already a decision node for that above.