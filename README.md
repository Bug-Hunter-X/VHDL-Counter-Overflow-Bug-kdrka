# VHDL Counter with Overflow Bug

This repository demonstrates a common bug in VHDL code related to counter overflow and provides a solution.

## Bug Description
The `buggy_counter.vhdl` file contains a counter that increments on each rising clock edge. However, the handling of the maximum count value (15 in this example) is flawed.  When `internal_count` reaches 15, the code resets it to 0.  While functionally this appears correct, the potential for subtle issues exist that may not surface immediately (especially in hardware implementations).

## Solution
The `fixed_counter.vhdl` demonstrates a corrected implementation.  Improvements include more robust handling of boundary conditions for improved clarity and reliability. 

## How to Run
You can use a VHDL simulator (such as ModelSim, GHDL, or others) to simulate both versions of the code and compare their behavior.  Look for differences in the `count` output, especially when the counter approaches and exceeds its maximum value. 