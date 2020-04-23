# CPE 1040 - Spring 2020 (IN PROGRESS)

Author: Ivo Georgiev, PhD  
Last updated: 2020-04-23   
Code: 9acff7cc344309ac25976869a50535751d4b970d      

![alt text](images/CPE-Asst6-Modulo-Ctr.jpg "Final circuit for CPE 1040 Asst 6")

This is lesson and assignment 007 for the Spring 2020 installment of the CPE 1040 - Intro to Computer Engineering course at MSU Denver.

**NOTE:** 
1. This lesson & assignment [README](README.md) is _intentionally_ blank, to be used as the **Lab Notebook** for the study & submission. _It is a great aid for your study and the main component of your submission._
2. Read and follow the [lesson-and-assignment](lesson-and-assignment.md).
2. Refer to the [submission template](submission-template.md) for formatting expectations and examples. 
4. Refer to the [criteria and guide](criteria-and-guide.md) for the different components of your submission.

## Take-home lab kit

The take-home lab kit is meant to provide continuity of our lab projects across the transition to online instruction. Please, read the [BOM, guide, and care document](https://docs.google.com/document/d/18IDsrQlZY_QkmWG7FFtGqd9M2S1wL8ShJrD00aHwBwQ/edit?usp=sharing) and use it as a reference throughout the lesson and assignment.

## Learning how to learn

The human mind is a very fine machine with amazing capabilities. And like any complex mechanism, it takes study to learn to use it effectively. This standalone section will contain practical information and advice for learning how to learn.

##### Learning How to Learn 03

1. The two-minute principle.    
   The _two-minute principle_ is an extremely easy and useful technique that requires no setup and no special circumstances. How often have you felt _stuck_ in indecision about how to proceed or even how to start, say, a piece of work, a homework, an exam review, or any other thing that you know you have to do but you feel reluctant to start or continue? And how often, for one reason or another, you have been startled out of this frozen state, only to find that you have seamlessly slid into the activity without noticing, and that all resistance has disappeared? In a way, you only had to start, to get yourself into a productive state of _flow_ instead?   
   
   TO DO: The two-minute principle is the simplest technique to do this at will. And that's all it is: one way or another you focus on what you have to do _for 2 minutes_ before you look up and reassess; more often than not, relieved of the pressure of having to _slog through_ "all this work that has piled up", it has jumped into the limited task at hand and bit into it. Chances are that in 2 minutes you will be in a completely different state of mind, able to tick tasks off without any negative emotions, but even with _excitement for every completed piece of work_.    
   
2. Mindset: fixed vs growth.    
   The term _mindset_ refers to the usual way you react to mental challenges. If you can't do something successfully, do you get frustrated and give up, or do you get frustrated and keep banging at it and try new things? A lot of research literature has accumulated that shows that the difference in our reactions to percieved adversity and our reflexive attribution of the difficulties to either _intrinsic ineptitude_ or _not enough training yet_ divide us into two fundamentally different behavioral groups. The former attribution is associated with the so called _fixed mindset_ and the latter with the so called _growth mindset_.
   
   TO DO: The worst thing you can do when you read the above paragraph is to conclude that you have the fixed mindset and that's that. The whole point of talking about mindsets is to convince you to try the other, the growth mindset, and realize that it takes no more effort than the other. It's just a matter of decision. Just like you have no problem deciding between orange chicken and mushrooms with greens at a Panda Express, you can choose to withhold any habitual thoughts of personal inadequacy, and all the fear and pain that such thoughts bring along, and just give it a shot: "I don't understand this, but I will give it some time, look at it from different angles, ask others to see how they think about it, and reassess later". At every moment when you are faced with something new - which in college happens regularly - stay conscious about how you react at the first encounter: are you calm and keep your mind free of extraneous emotions, so you can start thinking about the new thing; or do you try to distance yourself from it and hope it will pass you by? The former is the fixed mindset. The latter is the growth mindset. It's your choice, really.

## Lesson & Assignment 007: Logic gates (IN PROGRESS)

This is a lesson and assignment on _logic gates_. Logic gates are circuits which apply logical functions on their inputs and output the result. Logic gates can have 1 or more inputs but usually have only 1 output. They are the building blocks of modern computational hardware, including arithmetic, logic, and control circuits. The logic gates themselves are built out of transistors.

### Section 1: AND, OR, and NOT gates from NPN transistors

#### 1. Study

##### Logic levels
Logic gates are the crucial layer in the _hardware stack_ of a computer, in which continuous voltages are _discretized and abstracted_ into the 1s and 0s that represent _binary numbers_. While logic gates are implemented via complex _transistor-transistor logic_ or _diode-transistor logic_, their function is simple and can be understood in terms of just _functions of 0s and 1s_.

On the electrical level, _logic low_, commonly designated as `0`, is usually taken to be 0V or _ground_ (which is the common reference volgate for the whole circuit), and _logic high_, commonly designated at `1`, is the highest voltage at which the circuit operates. Common logic-high voltages in electronics are 3.3V and 5V. Other values in the range 1V-12V are less common.

The continuous voltage range between _logic low_ and _logic high_ is usually divided in 3 distinct bands:
- _logic low_: [0V, V<sup>low</sup><sub>max</sub>];
- intermediate forbidden: [V<sup>low</sup><sub>max</sub>, V<sup>high</sup><sub>min</sub>];
- _logic high_: [V<sup>high</sup><sub>min</sub>, V<sup>high</sup><sub>max</sub>], where V<sup>high</sup><sub>max</sub> is either 3.3V or 5V.

The intermediate band serves as a buffer, simplifying the recognition circuitry and filtering noise. The simplicity of dividing the voltage range into only 3 bands is also one of the chief advantages of _binary_ as the fundamental number system of computing.
   
##### Logical functions
Logic gates perform _functions_ (relations between input and output signals, in which there is a _single_ output for every _combination of outputs_) on signals that can take one of two values: _logic low_ (aka `0`, or `False`) and _logic high_ (aka `1`, or `True`). In other words, logical functions have the same _domain_ and _range_, equal to the discrete set of `{0, 1}`. (_Note that this is the notation for a **discrete** range. In our case, it consists of the set of numbers 0 and 1, and no others. **Continuous** ranges are represented with the following notation: `[0, 1)` (real-number interval, half-open on the right, including all real numbers between 0.0 and 1.0, excluding 1.0), `(0, 1]`, and `[0, 1]`._) Once we start talking about logic gates and design more complex computational circuits out of them, we forget about voltages, currents, and impedances. Thus, logic gates bridge the _electrical layer_ and the _logical layer_ in the _computer stack_.

The inputs of logic gates are all the combinations of the number of inputs, where each input is in the range `{0, 1}`. For example, a 2-input gate will have the following 4 possible different inputs: `00`, `01`, `10`, and `11`. What this means is that, if we designate the 2 inputs "A" and "B", the input combinations are all of the form "AB". (_Note that here we use the term "combinations" in a mathematically imprecise way, as what we are talking about are actually "permutations". For example, `10` and `01` are **distinct permutations** whereas they represent the **same combination**. That is, order matters for permutations and does not matter for combinations. Since we want the two inputs `10` and `01` to be distinct, we are really talking about permutations._) The single output of the 2-input gate is in the range `{0, 1}`.

##### Boolean algebra
An _algebra_ is a system of rules for the manipulation of a certain _set of mathematical entities_. By this definition, [_Boolean algebra_](https://mathworld.wolfram.com/BooleanAlgebra.html) is the algebra of the two-valued set `{0, 1}`. Mathematically, it is a _ring_, closed under the _meet_ (aka _AND_) and _join_ (aka _OR_) operations, and its two _literals_ are `0` and `1`, which are inverse of each other. Boolean algebra greatly simplifies the understanding, design, and verification of electronic circuits.

##### Truth tables
Because they are discrete-valued, with the only two values `0` and `1`, logic functions can very conveniently be represented as _truth tables_, which are exhaustive and explicit representation of the functional relationship between inputs and outputs. In fact, truth tables are used to _define_ the logic functions themselves. Here is a sampling:

A | B | /A (aka NOT) | AB (aka AND) | A+B (aka OR) | /(A+B) (aka NAND)
--- | --- | --- | --- | --- | ---
0 | 0 | 1 | 0 | 0 | 1
0 | 1 | 1 | 0 | 1 | 1
1 | 0 | 0 | 0 | 1 | 1
1 | 1 | 0 | 1 | 1 | 0    

###### Notation                                          
The symbol /A is equivalent to "A-bar" as in 
```
_
A
```
This means the _inverse_ of A. `1` is the inverse of `0`, and vice versa.

##### Logic gate internals
As can be seen on page 2 of the [AND gate datasheet IC](http://www.ti.com/lit/ds/symlink/sn74ls08.pdf), logic gates are internally implemented as transistor-and-diode cicuits, of which the two principle families are _transistor-transistor logic (TTL)_ and _diode-transistor logic (DTL)_. As we will see in the next part, a basic version of the three principal logic gates NOT, AND, and OR can be implemented with 1 (for NOT) or 2 (for AND and OR) NPN transistors. The industrial implementation looks so much more complicated because it has to meet requirements for _signal stability_, _switching speed_, _drive capability_, and various other parameters, all of which are listed in the [datasheet](http://www.ti.com/lit/ds/symlink/sn74ls08.pdf).

#### 2. Apply
1. Using the axioms of Boolean algebra, prove/derive/show [DeMorgan's Laws](https://en.wikipedia.org/wiki/De_Morgan%27s_laws). This exercise provides a very stable kernel of understanding of Boolean algebra and logical circuits.
2. Using 1 NPN transistor, an LED, and appropriate resistors, build an _inverter_ (aka NOT) gate. In partcular, when the base of the transistor is at 0V, the LED has to be ON, and, vice versa, when the base is at 5V, the LED has to be OFF. Feel free to follow [this guide](https://www.petervis.com/Education/logic-gates/transistor-logic-not-gate-inverter.html). _Hint: The two resistors have to be matched. Since we haven't provided 1K Ohm resistors, and the 10K Ohm ones limit the current too much, you can use 3 x 220 Ohm resistors for the base, and 2 x 220 Ohm ones for the collector load, both **in series**._
3. Using 2 NPN transistors, on LED, and appropriate resistors, build and OR gate. In particular, when both bases are at 0V, the LED should be OFF, and when at least one base is at 5V, the LED should be ON. _Hint: Think of our basic NPN circuit with 10K Ohm at the base and a resistor-and-LED load on the collector. What if you build a second NPN subcircuit as a mirror of "acorss" the first one, and connect the collectors of both together? Try to draw the circuit before you look it up on the [Internet](#logic-gates)._
4. The previous 3 circuits could be driven by just plugging the wire at the base (with a 10K resistor!) directly into the 5V or 0V rail. Now take two converter channels and run the base wires over to the micro:bit. Connect to two digital output pins.
5. Write a program that:
   1. Drives the two inputs (1 input for NOT) of the gate. _Note that thes are output pins for the micro:bit._
   2. It uses the two LEDs at the top-left of the micro:bit matrix to indicate the input levels. That is, the LED at `(0, 0)` should represent the "A" input, and the LED at `(1, 0)` should represent the "B" input. Use brightness 5 for `0` and brightness 255 for `1`. The two LEDs "AB" should correspond to the two digital output pin values that drive the gate through the voltage converter.
   3. Cycles through the 4 input combinations in the order: `00`, `01`, `10`, and `11`.

#### 3. Present

In the [Lab Notebook](README.md), include:
1. A short narrative about the experiment.
2. The derivation of DeMorgan's Laws drawn on paper or rendered in mathematical notation, in an image.
3. Short video of the operation of the circuit from 1.2.2.
3. Short video of the operation of the circuit from 1.2.3.
4. Short video of the operation of the circuit from 1.2.4.
5. Short video of the operation of each of the circuits from 2.2.5. _Hint: You can build them side by side and only switch the base inputs across._

In the [repository](./), include:
1. File `microbit-program-1-2-5.js` with the code you used in task 1.2.5.

### Section 2: Drive and read a gate with the micro:bit (IN PROGRESS)

#### 1. Study
- where is the "output"
- voltage at the output

#### 2. Apply
- measure the output voltage
- feed back into micro:bit as input pin: (i) analog, and (ii) ditigal
- display as 0 or 1 on LED matrix

#### 3. Present
- writeup on voltage levels
- videos of the circuits operating
- programs used

### Section 3: Logic gate ICs (IN PROGRESS)

#### 1. Study
- reading the datasheets
- how logic gates are actually built
- correct placement and powering of the log gates
- how much load can the logic gates drive

#### 2. Apply
- for each logic gate, exchange the NPN circuit from Seciton 2 with a corresponding IC gate
- measure the voltage levels on both sides (3.3V and 5V)

#### 3. Present
- equivalent to previous: measurements and video

### Section 4: Combinational logic (IN PROGRESS)

#### 1. Study
- another pass of Boolean algebra and truth tables
- functional sets: OR+NOT, AND+NOT, NAND, NOR
- combinational logic: vs sequential, propagation delay, logic minimization

#### 2. Apply
- compose combinational ciruits to build AND out of OR+NOT, OR out of AND+NOT
- compose combinational ciruits to build AND, OR, and NOT out of NAND
- compose combinational ciruits to build XOR out of NAND
- drive with the micro:bit (input signals)
- build direct and combinational next to each other and verify same output: (i) with an AND gate and an LED load, (ii) micro:bit

#### 3. Present
- writeup with derivations, truth tables
- videos of circuits operating
- programs used

### Section 5: Truth table on the micro:bit (IN PROGRESS)

#### 1. Study
- truth table as a definition of a logic function
- next to each other with 2 inputs: is there an output (function) that is missing?
- more than two inputs
- minimization and a glimpse of Karnaugh maps
- multiplexors are a major element of combinational control ciruits.

#### 2. Apply
- write a logic verifier program for the micro:bit
- it should identify and name the logic function of a gate IC or combination
- drive the multiplexor of the XOR/XNOR gate and verify through operation

#### 3. Present
- anwers to questions
- programs written
- videos of circuits operating

### Section 6: Bi-directional 3-bit binary ripple counter (asynchronous) (IN PROGRESS)

#### 1. Study
- synchronous vs asynchronous
- ripple & delays
- down schematic, up schematic, derive control
- different ways to build a multiplexer

#### 2. Apply
- remove the MSB of the counter to free a converter channel
- built a multiplexer from gates
- drive the selector from the micro:bit

#### 3. Present
- design writeup, including truth table
- program source
- video

### Section 7: Bi-directional synchronous circuits (IN PROGRESS)

#### 1. Study
- pros and cons of synchronous and asynchronous (not just counters)
- timing in ciruits (datasheets, levels of abstraction)

#### 2. Apply
- build a 3-bit synchronous up counter
- build a 2-bit up/down multiplexed synchronous counter
- build a 3-bit left/right shifter out of 3 D-flip-flops (control?)

#### 3. Present
- timing diagrams and schematics
- programs
- videos

### Section 8: Synchronous modulo counters (IN PROGRESS)

#### 1. Study
- encoding and decoding
- binary numbers and control circuits

#### 2. Apply
- 3-bit upmod-5 counter (local reset)
- 3-bit down mod-6 counter (local reset)
(- 3-bit circuit that cycles through the sequence 0-1-2-3-4-5-4-3-2-1-0-1-2-3-4-5-6-5-4-3-2-1-0-...)
- if it can't fit, remove one flip-flop chip, and do 0-1-2-**3**-2-1-0-1-**2**-1-0-... (opens up a control signal from micro:bit)

1. Build a [_combinational circuit_](https://www.electronics-tutorials.ws/combination/comb_1.html) out of [_logic gate_](https://en.wikipedia.org/wiki/Logic_gate) [ICs](https://en.wikipedia.org/wiki/List_of_7400-series_integrated_circuits) (AND, OR, NOT, etc.) to drive one of the control signals to change your circuit from a mod-8 counter to a **mod-5 counter**:
   1. Design the signal necessary to force the counter to cycle back to `000` before it reaches `101`.
   2. Ask staff for the logic gates you need. _We have a variety of [74LS00 chips](https://en.wikipedia.org/wiki/List_of_7400-series_integrated_circuits)._
   3. Build the circuit. _Note: Don't forget to power and ground the ICs._
2. Record a video showing mod-5 counting and link in README.
3. Now disconnect the combinatorial circuit and modify your program to do the same thing with the clear control signal that comes from the micro:bit.
4. Commit to your repository as file `mod-5-clr.js`.
5. Record a video showing mod-5 counter without external logic gates, and link to README with a brief explanation of your code.

#### 3. Present
- diagrams, schematics, control circuit designs
- programs
- videos

## Resources

### micro:bit 

1. [micro:bit lessons](https://makecode.microbit.org/lessons).
2. [micro:bit ideas](https://microbit.org/ideas/).
3. A list of some more [advanced projects](https://www.itpro.co.uk/desktop-hardware/26289/13-top-bbc-micro-bit-projects).
4. The [projects](https://github.com/carlosperate/awesome-microbit#%EF%B8%8F-projects) at the [awesome micro:bit list](https://github.com/carlosperate/awesome-microbit).
5. micro:bit [technical documentation](https://tech.microbit.org/).
6. micro:bit [reference](https://makecode.microbit.org/reference/), and [pins](https://makecode.microbit.org/reference/pins/servo-set-pulse), specifically.

### Transistors
1. Video of [transistor operation](https://www.youtube.com/watch?v=7ukDKVHnac4)
2. Video of [PN diode operation](https://www.youtube.com/watch?v=-SSkjWuUri4)
3. Video of [NPN and PNP transistor operation](https://www.youtube.com/watch?v=R0Uy4EL4xWs)
4. Video of [NPN vs. PNP Transistors as Common-Emitter Switches](https://www.youtube.com/watch?v=kNVaIqmKUoI)
5. Video of [semiconductor operation](https://www.youtube.com/watch?v=33vbFFFn04k) by Ben Eater.
6. Video of [transistor operation](https://www.youtube.com/watch?v=DXvAlwMAxiA) by Ben Eater.
7. Video of [MOSFET operation](https://www.youtube.com/watch?v=stM8dgcY1CA)

#### Transistor datasheets

1. NPN transistor [2N3904 datasheet](https://www.sparkfun.com/datasheets/Components/2N3904.pdf)
2. PNP Transistor [2N3906 datasheet](https://www.sparkfun.com/datasheets/Components/2N3906.pdf)

### Logic gates

1. Vodeo of [logic gates out of transistors](https://www.youtube.com/watch?v=SW2Bwc17_wA). Note, this is an implementation with MOSFET transistors, which, in conctrast to BJTs, have no base current but operate on the principle of a _voltage-regulated gate_.
2. Video tutorial of [BJT and MOSFET transistors](https://www.youtube.com/watch?v=EBcSqrRby_Y) side-by-side.
2. Video tutorial for [building logic gates out of transistors](https://www.youtube.com/watch?v=sTu3LwpF6XI&t=435s)

#### Logic gate datasheets

1. See the [BOM](https://docs.google.com/document/d/18IDsrQlZY_QkmWG7FFtGqd9M2S1wL8ShJrD00aHwBwQ/edit#heading=h.o3s6rnopwwhc) of the take-home lab kit.

### Flip-flops
1. Very in-depth yet accessible Wikipedia article on [flip-flops](https://en.wikipedia.org/wiki/Flip-flop_(electronics))
2. Video of [flip-flop circuit build & operation](https://www.youtube.com/watch?v=IykOrxVcdyg)

#### Flip-flop datasheets

1. D-type flip-flop [74LS74](http://www.ti.com/lit/ds/symlink/sn74ls74a.pdf)

### Capacitors

1. A short lesson and video on [how a capacitor works](https://www.build-electronic-circuits.com/how-does-a-capacitor-work/)

### Sensors

1. SparkFun soil moisture sensor [hookup guide](https://learn.sparkfun.com/tutorials/soil-moisture-sensor-hookup-guide). _Note: The guide is for Arduino, not micro:bit, but that does not affect the operation of the sensor See the intro item in the [soil sensor section above](#soil-sensor)._

### Logic level converter

1. [Bi-directional logic level converter](https://www.sparkfun.com/products/12009) between 3.3V and 5V.
2. Converter [schematic](https://cdn.sparkfun.com/datasheets/BreakoutBoards/Logic_Level_Bidirectional.pdf), N-channel MOSFET [datasheet](https://cdn.sparkfun.com/datasheets/BreakoutBoards/BSS138.pdf), with [operation explanation](https://cdn.sparkfun.com/tutorialimages/BD-LogicLevelConverter/an97055.pdf), and **most importantly** [hookup guide](https://learn.sparkfun.com/tutorials/bi-directional-logic-level-converter-hookup-guide).

### Oscilloscopes

1. Video [Oscilloscopes Made Easy Part 1](https://www.youtube.com/watch?v=uU3FhH7_MWo&t=1s)
2. Video [EEVblog #279 - How not to blow up your oscilloscope](https://www.youtube.com/watch?v=xaELqAo4kkQ)
3. Video [Oscilloscopes Made Easy Part 2](https://www.youtube.com/watch?v=5VyotIVwRiA)
4. Video [How to use an oscilloscope (SparkFun)](https://www.youtube.com/watch?v=u4zyptPLlJI)
5. Video [Oscilloscope tutorial](https://www.youtube.com/watch?v=CzY2abWCVTY)
6. Video [Rigol 1000s Series docs (manuals, datasheets, videos)](https://www.rigolna.com/products/digital-oscilloscopes/1000z/)

### Github

1. Github Tutorial for Beginners ([webpage](https://product.hubspot.com/blog/git-and-github-tutorial-for-beginners)).
2. Github Basics for Mac and Windows ([video](https://www.youtube.com/watch?v=0fKg7e37bQE)).
3. git & Github Crash Course for Beginners ([video](https://www.youtube.com/watch?v=SWYqp7iY_Tc)).
4. Introduction to Github for Beginners ([video](https://www.youtube.com/watch?v=fQLK8Ib_SKk)).
5. About `git` ([webpage](https://git-scm.com/about)).
6. `git` [documentation](https://git-scm.com/doc) (webpage, book, videos, reference manual).
7. [Github markdown cheat sheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).

### JavaScript

1. Technically, the language which is used side-by-side with Blocks in the Makecode ronment is a subset of [TypeScript](https://makecode.com/language), which itself is a superset of JavaScript (technically, [ECMAScript](https://www.ecma-international.org/ecma-262/10.0/index.html#Title)), with some JS features not implemented in Makecode.
2. The limited [JavaScript mini-tutorial](https://makecode.microbit.org/javascript) in Makecode.
3. Official [TypeScript documentation](https://www.typescriptlang.org/docs/home.html):
   1. TypeScript in 5 min [tutorial](https://www.typescriptlang.org/docs/handbook/typescript-in-5-minutes.html). _Note: You will need to [download](https://www.typescriptlang.org/index.html#download-links) and install an integrated development environment (IDE). The two that I recommend are Visual Studio Code from Microsoft and WebStorm from JetBrains._
   2. The full documentation and reference is under _Handbook_. Bear in mind that you are drinking from the hose. Don't be surprised if not everything is presented in a strictly incremental manner.
4. In-browser TypeScript [playground](https://www.typescriptlang.org/play/index.html). Note that micro:bit specific code will not run, but you can still play. _Start making the distinction between a generic multi-purpose programming language (TypeScript) and functionality (packages, libraries, objects, etc.) that is specific to a particular device (micro:bit), though written in the same programming language._
5. A pretty good and very palatable JS tutorial with in-browser coding, by [Codecademy](https://www.codecademy.com/learn/introduction-to-javascript).
6. Extensive and detailed [JS tutorial](https://javascript.info/), with some advanced material thrown in. **I like this one!**
7. The most authoritative JS resource on the Web, including tutorials and reference, by [Mozilla](https://developer.mozilla.org/en-US/docs/Web/JavaScript).
