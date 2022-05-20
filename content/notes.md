+++
title = "Talk Summaries"
+++

These notes have been taken from the [Google
Docs](https://docs.google.com/document/d/1ms4O6HDtlIHP6hnKWlNQhAeniiqKsIKuB6nRMwPRHSg/edit?usp=sharing),
which was edited live during the workshop.

### Designing memory architectures with high-level synthesis: What could possibly go wrong?

by [Christian Pilato](https://pilato.faculty.polimi.it/), Politecnico di Milano.

#### Notes

- Timing specifications not captured in interface description in verilog (i.e. input 1 should arrive
  1 cycle after input 2)
- Using MLIR as an intermediate step, with various different input flows for different languages, to
  then target different outputs.
- High focus on optimising memory architecture and usage to produce high-bandwidth memory
  architectures.
- Generate C++ from MLIR to reuse existing high-level synthesis tools.
- High-level synthesis does not necessarily have to be for software programmers to target hardware
  without knowing hardware design.  Any DSL that makes it easier to generate hardware can be called
  HLS.

#### Questions/Comments

- This project name is unfortunate given Microsoft’s [Project
  Everest](https://www.microsoft.com/en-us/research/project/project-everest-verified-secure-implementations-https-ecosystem/)
  and the first github hit doesn’t look like it is this

### Optimizing Large Integer Multiplication in HLS using Equality Saturation

by [Ecenur Üstün](http://people.ece.cornell.edu/eu49/), Cornell.

#### Notes

- The ideal hardware design with HLS would allow for tighter design space iteration in HLS without
having to go through synthesis.
- E-graphs can be helpful with generating all possible combinations of equivalent expressions and
choosing the right ones.

#### Questions/Comments

- How does this methodology compare to the Xilinx-published Ultrafast and HLS methodology? (slide 4)
- Is something like an SVD or genetic algorithm needed given the variable cost estimations? Is this
  actually a case where ML could help? (Slide 11/12) – this work focused on achieving the Pareto
  frontier for the single optimization

### Time-Sensitive Interfaces for Hardware Modules

by [Rachit Nigam](https://rachitnigam.com/), Cornell.

#### Notes

Timing specifications not captured in interface description in verilog (i.e. input 1 should arrive 1
  cycle after input 2).

#### Questions/Comments

- If I wanted to write a multacc where the latency was a parameter (i.e. so I could target different
  frequencies) could I write @[t+OFFSET, t+OFFSET+1] for the output?
- By including the timing information in the design code, you’re now tying together verification
  with the design. How does this interact with blocks generated in other languages (e.g. vendor IP)?
- How does component state (beyond pipeline registers) interact with this interface?  I.e. if we
  have a module that has one input and outputs the cumulative sum of received inputs how would we
  express that? (Rachit just explained how this is done, so no need to ask).  (There is an explicit
  way to express a register that moves data from one time position to another).
- Comment: Being able to catch all these errors at compile time rather than digging through
  waveforms is very valuable.  Also when using other people’s modules it’s valuable for the
  interface to be as explicit as possible.  I also like that when writing a formal specification for
  the module, the timing information wouldn’t be in the specification but in the module’s interface.
- Only addition was shown as being needed in the interface, but would other more complicated
  expressions be needed sometimes?
