# CMOS Full Adder Design and Simulation

This repository contains the circuit design and simulation results for a 1-bit Full Adder implemented using Complementary Metal-Oxide-Semiconductor (CMOS) logic. 

## Repository Contents

*   **`full_adder_cmos.pdf`**: Contains the detailed schematic diagram of the CMOS full adder circuit, built using a 28-transistor (28T) architecture.
*   **`full_adder_sim.pdf`**: Contains the transient simulation waveforms verifying the truth table and time-domain logic functionality.

## Theory & Circuit Operation

A Full Adder is a fundamental digital logic component that performs the arithmetic addition of three 1-bit binary numbers: two significant bits ($A$ and $B$) and a carry-in bit ($C_{in}$). It generates two outputs: a Sum ($Sum$) and a Carry-out ($C_{out}$).

### Truth Table
| A | B | $C_{in}$ | Sum | $C_{out}$ |
|---|---|---|---|---|
| 0 | 0 | 0 | 0 | 0 |
| 0 | 0 | 1 | 1 | 0 |
| 0 | 1 | 0 | 1 | 0 |
| 0 | 1 | 1 | 0 | 1 |
| 1 | 0 | 0 | 1 | 0 |
| 1 | 0 | 1 | 0 | 1 |
| 1 | 1 | 0 | 0 | 1 |
| 1 | 1 | 1 | 1 | 1 |

### Boolean Expressions
The standard logic expressions for the outputs are:
*   **Sum:** $Sum = A \oplus B \oplus C_{in}$
*   **Carry-out:** $C_{out} = A \cdot B + C_{in} \cdot (A + B)$

### CMOS Implementation Details
In a standard static CMOS design, logic equations are realized using a Pull-Up Network (PUN) constructed with PMOS transistors and a Pull-Down Network (PDN) constructed with NMOS transistors.

*   **28T Architecture:** The schematic in this project utilizes a standard 28-transistor configuration (14 PMOS and 14 NMOS). You can observe these labeled from $M1$ to $M28$ in the circuit diagram.
*   **Complex Gates:** Instead of cascading standard discrete gates (like separate XOR and AND gates), this design uses complex compound logic to directly implement the Sum and Carry logic, which optimizes the overall transistor count and reduces propagation delay.
*   **Advantages:** This static CMOS approach ensures virtually zero static power consumption (as there is no direct path between power and ground during steady states) and provides excellent noise margins, making it ideal for integrated circuit configurations.

## How to View
Click on the respective `.pdf` files in the repository above to view the high-resolution circuit blueprints and their corresponding simulation results directly within your browser.
