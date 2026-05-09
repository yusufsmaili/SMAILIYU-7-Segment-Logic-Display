# SMAILIYU 7-Segment Logic Display

This project implements a custom 7-segment display sequence for the name **SMAILIYU** using discrete digital logic.

The circuit uses a **555 timer** as the clock source, a **7493 binary counter** to generate the 3-bit input states, and **74LS logic gates** to drive a common-cathode 7-segment display.

## Project Overview

The system cycles through eight counter states:

| Counter State | Displayed Letter |
|---|---|
| 000 | S |
| 001 | M |
| 010 | A |
| 011 | I |
| 100 | L |
| 101 | I |
| 110 | Y |
| 111 | U |

Because a standard 7-segment display cannot form a perfect letter **M**, the M is represented using a 7-segment approximation.

## Digital Design Flow

This project follows a classical digital design process:

1. Define the display specification
2. Create the truth table
3. Derive Boolean equations
4. Implement the logic using gates
5. Verify the design in simulation
6. Build the physical circuit on a breadboard

## Boolean Equations

```text
a = A'B' + A'C'
b = B + C
c = A' + B + C
d = AB + B'C'
e = ABC + AB'C' + A'BC' + A'B'C
f = C' + AB + A'B'
g = BC' + A'C'
