+++
title = "Talk Summaries"
+++

### Designing memory architectures with high-level synthesis: What could possibly go wrong?

by [Christian Pilato](https://pilato.faculty.polimi.it/), Politecnico di Milano

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
