---
layout: home
title: ISA
nav_order: 3
---

# ISA

A PRTVM implementation can support various subsets of instructions

1. **B**ase (the bare minimum, CLI capabilities)
2. **M**ath (advanced mathematics capabilties)
3. **G**raphical (rendering with OpenGL)
4. **F**ile (file I/O operations)
5. **N**etwork (network I/O operations)
6. **O**S (accessing the OS directly)

Similar to Risc-V, these letters showcase what features are supported. A feature-complete PRTVM implementation would be labelled as `BMGFNO`. `B` can be omitted, as it is the bare baseline to be considered useful.