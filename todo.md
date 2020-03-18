
# Conversion to Take-Home TODOs

1. ~Turn into a lesson-n-assignment:~
   1. ~Divide each section into study-apply-present parts.~
   2. ~Structure lesson and assignment in parallel, section by section.~
   3. ~Interleave the exposure and exploration parts. It should be a single progression.~
   4. ~Reference videos and materials _inline_.~
   5. ~Supplement with _short_ original videos.~
   6. ~Overview should state this format and identify prerequisites. (Link with previous.)~
   7. ~Link to [lesson 6](https://docs.google.com/document/d/1TiirGwXiKg6ehxjVPpW-ISQryf8eqycvG4PZMq8cm2U/edit?usp=sharing).~
   8. ~Include a Learning How to Learn section at the very beginning and weave into [Introduction](#overview).~
   3. ~Separate lab-kit doc:~
      1. ~Include lab-kit contents, user guide, and safety of operation. Link this l&a to new document.~
      2. ~Include video and/or guide for using handheld multimeters.~
1. ~No workstation, so no buttons or logic output LEDs. Adapt to use the micro:bit button and LEDs.~
4. ~Add note that 74LS00 chips require 5V.~
5. Square wave gen in micro:bit:
   1. In separate `forever` loop. A note on _threads and fibers_. Link to [Reactive](https://makecode.microbit.org/device/reactive).
   2. Test the following functions (_Use in conjunction to test w/o oscilloscope._): 
      1. [`analogSetPeriod`](https://makecode.microbit.org/reference/pins/analog-set-period),
      2. [`onPulsed`](https://makecode.microbit.org/reference/pins/on-pulsed),
      3. [`analogSetPitchPin`](https://makecode.microbit.org/reference/pins/analog-set-pitch-pin),
      4. [`analogPitch`](https://makecode.microbit.org/reference/pins/analog-pitch)
      5. [`pulseDuration`](https://makecode.microbit.org/reference/pins/pulse-duration)
   3. Discover and show all the pin simulation functions of the MakeCode environment.
8. Note that at most 4 lines can be voltage converted. _The /CLR signal is active-low. If 3.3V is enough to keep it in the high state, it can be connected directly._
9. ~Explain both voltage converter devices.~
10. Build the final circuit, check the constraints with translation pins, and update the "front-page" picture.
11. Remove lab oscilloscope parts and maybe explore the [microbit as an oscilloscope project](http://www.elektronik-labor.de/Microbit/Microbit9.html).


