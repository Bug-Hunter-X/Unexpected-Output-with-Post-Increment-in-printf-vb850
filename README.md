# Unexpected Output with Post-Increment in printf
This repository demonstrates a subtle C code bug related to the post-increment operator (`++`) used within a `printf` function call. The code produces an output that might be counterintuitive to programmers not fully aware of how the post-increment operator interacts with function argument evaluation.

## Bug Description
The primary issue lies in the order of evaluation of function arguments and the behavior of the post-increment operator.  The post-increment operator increments the variable *after* its value has been used in the expression.

## How to Reproduce
1. Compile the code using a C compiler (e.g., GCC):  `gcc bug.c -o bug`
2. Run the executable: `./bug`
3. Observe the output, which may differ from what is initially expected.

## Solution
The provided `bugSolution.c` file addresses the issue by demonstrating safer and more explicit ways to handle the post-increment operator in similar situations.  The solution shows how to achieve clearer and more predictable results.

## Learning Points
This example highlights the importance of understanding operator precedence and the order of evaluation in C, especially when working with side effects like increment/decrement operators within function calls.