# Uncommon Ada Bug: Array Modification within Loop

This repository demonstrates a subtle bug that can occur in Ada when modifying an array element within a loop. The bug is not immediately obvious but can lead to unexpected behavior or runtime errors. The example shows how changes made to the array during iteration may affect the loop's control flow or access to other array elements.

## Bug Description:
The bug arises from the interaction of modifying an array's element while iterating over it using a `for` loop. In the provided `bug.ada` file, the loop iterates through an array. If a specific condition is met (element equals 5), the element is modified and the loop exits. This might seem straightforward, however, this action can cause unexpected consequences in more complex scenarios where array access might depend on the loop's index and the array's changing state during iteration. 

## Solution:
The provided solution demonstrates a safer approach to modifying arrays within loops, ensuring that such modifications don't lead to index issues or unintended behavior. The `bugSolution.ada` file shows an improved way to manage the modification and loop, reducing the risks associated with the bug.

## How to Reproduce:
1. Compile and run `bug.ada`. Observe the output.
2. Compile and run `bugSolution.ada` and compare the output with the previous one.  The `bugSolution.ada` offers a safer approach to avoid this common pitfall.

## Note:
This demonstrates a simple case, but similar issues can appear in more complex scenarios involving nested loops or concurrent access to arrays.