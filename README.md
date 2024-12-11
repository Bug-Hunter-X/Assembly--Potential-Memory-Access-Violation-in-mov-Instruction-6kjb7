# Assembly: Potential Memory Access Violation

This repository demonstrates a potential memory access violation in an assembly instruction and provides a solution.

The `bug.asm` file contains the faulty code, which might result in an access violation if the `ecx` register exceeds allowed bounds. The `bugSolution.asm` file offers a solution with bounds checking to prevent the memory access violation.

## Bug Description:
The `mov eax, [ebx+ecx*4]` instruction calculates a memory address based on the values of `ebx` and `ecx`.  If `ecx` is too large, this calculation may exceed available memory, leading to a crash.

## Solution:
The solution involves checking the bounds of `ecx` before performing the memory access. This check prevents potential overflows and keeps the program from crashing.