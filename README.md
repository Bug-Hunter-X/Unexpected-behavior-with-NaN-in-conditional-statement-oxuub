# Unexpected NaN behavior in JavaScript conditional
This repository demonstrates a subtle bug in JavaScript related to the handling of NaN (Not a Number) in conditional statements.  The `foo` function intends to categorize numbers as positive, negative, or null.  However, NaN produces an unexpected result due to how JavaScript compares values involving NaN.

## Bug Description
The function incorrectly classifies NaN as a positive number.  This is because any comparison with NaN (including ===, !==, <, >, <=, >=) always results in `false`.  The `else` block is therefore executed. 

## Solution
The solution involves explicitly checking for NaN using `isNaN()` before performing other comparisons.