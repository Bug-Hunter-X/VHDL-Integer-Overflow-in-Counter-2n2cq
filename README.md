# VHDL Integer Overflow Bug

This repository demonstrates a common error in VHDL code: integer overflow in a counter.  The `buggy_counter.vhdl` file contains a counter that uses the `integer` data type.  When the counter reaches its maximum value (15 in this case), it will overflow, leading to unpredictable behavior.  The `fixed_counter.vhdl` demonstrates a corrected version using `unsigned` which avoids this issue.

## Reproducing the Bug

1. Simulate `buggy_counter.vhdl`. 
2. Observe the counter's behavior when it reaches its maximum value (15).  You will likely see unexpected results or simulation errors depending on the simulator.

## Solution

The `fixed_counter.vhdl` shows how to correct the problem by using `unsigned` instead of `integer`.  `unsigned` is specifically designed for representing numbers without the potential for signed integer overflow.