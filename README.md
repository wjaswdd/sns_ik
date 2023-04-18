# SNS-IK Library
`Version 0.2.3 beta`

The Saturation in the Null-Space (SNS) Inverse-Kinematics (IK) Library
implements a collection of algorithms written by Fabrizio Flacco for
inverting the differential kinematics of a robot.

## What problems are solved by this library?

The SNS-IK library is a library that is designed to compute fast solutions to
inverse-kinematics problems on redundant kinematic chains.
It is particularly good at handling multiple prioritized task objectives
while satisfying joint position and velocity limits.

The core solvers in this library operate at the velocity-level, although we
also include a position-level solver.
SNS-IK库是一个用于计算冗余运动链上逆运动学问题的快速解决方案的库。它特别擅长处理多个优先任务目标，同时满足联合位置和速度限制。
该库中的核心解算器在速度级别上运行，尽管我们也包括位置级别的解算器。
## Algorithm Overview:

**SNS Velocity IK:** This is the core algorithm developed by Fabrizio.
All of the other algorithms in this library are improvements upon this one.

**Optimal SNS:** Add an objective function to the standard SNS velocity IK solver,
allowing it to compute a solution that is both feasible and optimal.

**Optimal SNS with Margin:** Improvement upon the Optimal SNS solver to make it
better at avoiding discontinuous velocities over a sequence of IK calls.

**Fast SNS IK:** Several numerical improvements to reduce the total CPU time
required for the SNS Velocity IK solver.

**Fast Optimal SNS:** Similar to the Optimal SNS, but with several numerical improvements.

## References:

The algorithms in this library are drawn from three papers,
all written by the same team of three authors:
- Fabrizio Flacco
- Alessandro De Luca
- Oussama Khatib

The primary reference is:
- *Control of Redundant Robots Under Hard Joint Constraint: Saturation in the Null Space*
([.pdf](https://pdfs.semanticscholar.org/97ad/e6bad155d443e40f7b99d9773881b73a6ebc.pdf))
([IEEE](https://ieeexplore.ieee.org/document/7097068/)).
([video](https://youtu.be/Zm60jBdP-xs))

These two earlier papers are also relevant:
- *Prioritized multi-task motion control of redundant robots under hard joint constraints*
([.pdf](https://cs.stanford.edu/groups/manips/publications/pdfs/Flacco_2012.pdf))
([IEEE](https://ieeexplore.ieee.org/document/6385619/)).
- *Motion control of redundant robots under joint constraints: Saturation in the Null Space*
([.pdf](http://www.diag.uniroma1.it/~labrob/pub/papers/ICRA12_RedundancySNS.pdf))
([IEEE](https://ieeexplore.ieee.org/document/6225376/)).

## Contributors

**Original Library:**
```
Fabrizio Flacco
Dipartimento di Ingegneria Informatica, Automatica e Gestionale (DIAG)
Università di Roma "La Sapienza"
Rome, Italy
```
**Maintainence and Updates:**
````
Forrest Rogers-Marcovitz, Ian McMahon, and Matthew Kelly
Rethink Robotics
Boston, MA, USA
````
