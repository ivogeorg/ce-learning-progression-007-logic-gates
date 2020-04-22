# CPE 1040 - Spring 2020 (IN PROGRESS)

Author: Ivo Georgiev, PhD  
Last updated: 2020-04-22   
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
- Logic levels
- Logical functions
- Boolean algebra
- Truth tables
- Logic gates out of transistors (videos)

#### 2. Apply
- build NOT from 1 NPN transistor (R+LED load)
- build AND from 2 NPN transistors (R+LED load)
- build OR from 2 NPN transistors (R+LED load)
- drive the base from the micro:bit

#### 3. Present
- videos of the circuits operating

### Section 2: Drive and read a gate with the micro:bit

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

### Section 3: Logic gate ICs

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

### Section 4: Combinational logic

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

### Section 5: Truth table on the micro:bit

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

### Section 6: Bi-directional 3-bit binary ripple counter (asynchronous)

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

### Section 7: Bi-directional synchronous circuits

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

### Section 8: Bi-directional synchronous modulo counters

#### 1. Study
- encoding and decoding
- binary numbers and control circuits

#### 2. Apply
- 3-bit upmod-5 counter (local reset)
- 3-bit down mod-6 counter (local reset)
(- 3-bit circuit that cycles through the sequence 0-1-2-3-4-5-4-3-2-1-0-1-2-3-4-5-6-5-4-3-2-1-0-...)
- if it can't fit, remove one flip-flop chip, and do 0-1-2-3-2-1-0-1-2-1-0-... (opens up a control signal from micro:bit)

**TODO:** Can the last one fit on the long breadboard?

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

**TODO**

#### Logic gate datasheets

**TODO**

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
