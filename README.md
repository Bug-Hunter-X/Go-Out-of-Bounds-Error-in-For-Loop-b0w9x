# Go Out of Bounds Error in For Loop
This repository demonstrates a common out of bounds error in Go and its solution. The error arises when the loop counter exceeds the valid index range of an array or slice.

## Bug
The `bug.go` file contains a function `myFunc` that iterates over a slice of integers. The loop condition `i <= len(a)` causes an out of bounds error because the valid indices range from 0 to `len(a) -1`. When `i` reaches `len(a)`, accessing `a[i]` leads to a runtime panic.

## Solution
The `bugSolution.go` file corrects this error by modifying the loop condition to `i < len(a)`. This ensures the loop iterates only within the valid index range.

## How to reproduce
1. Clone the repository.
2. Navigate to the repository directory.
3. Run the `bug.go` file. Observe the runtime panic.
4. Run the `bugSolution.go` file. Observe the correct output without any errors. 