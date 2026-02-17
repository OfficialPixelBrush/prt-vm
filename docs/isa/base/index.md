---
layout: home
title: Base
nav_order: 1
parent: ISA
---

# ISA (Base)

Base instructions for the basis of PRTVM.

## Registers

| Name | Purpose | Width (Bits) |
| --- | --- | --- |
| `I0 - I12` | Integer  Register | 64 |
| `I13` (PC) | Program Counter | 64 |
| `I14` (SP) | Stack Pointer | 64 |
| `I15` (MP) | Memory Pointer, used for heap | 64 |
| `F0 - F7` | General Purpose Floating-Point Register | 32 |
| `D8 - D15` | General Purpose Floating-Point Register | 64 |

## Load/Move

| Mnemonic | Purpose |
| --- | --- |
| `MOV Tx,Ty` | Move value in `Tx` to `Ty` |
| `MOV [Tx],Ty` | Move value pointed at by `Tx` to `Ty` |
| `MOV Tx,[Ty]` | Move value in `Tx` to the address pointed at by `Ty` |

### Casting
Any of the `MOV` instructions copy the values from a float-register to an integer-register bitwise. Replacing the Mnemonic `MOV` with `CAST` instead performs a cast to the relevant type.

If the specified register is too small to hold the passed value, the value will just have the lower part that fits passed in.