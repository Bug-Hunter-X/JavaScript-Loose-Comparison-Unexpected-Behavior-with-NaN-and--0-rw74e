# JavaScript Loose Comparison Unexpected Behavior with NaN and -0

This repository demonstrates an uncommon issue in JavaScript's loose comparison (`==`) operator, specifically related to how it handles `NaN` (Not a Number) and `-0` (negative zero).

## The Bug

JavaScript's loose comparison (`==`) does not follow the standard rules of equality in all cases.  The primary issues here are:

1. **NaN Equality:** `NaN` is never equal to itself, even when using `==`.
2. **-0 Equality:** `0` and `-0` are considered equal by `==`.

This behavior can lead to unexpected results and difficult-to-debug errors in certain circumstances.

## Solution

To avoid these problems, always use strict equality (`===`) instead of loose equality (`==`). Strict equality correctly handles `NaN` and distinguishes between `0` and `-0`.

## How to reproduce

Clone the repository and run the `bug.js` file. You'll observe the unexpected results demonstrated in the code comments. Then run `bugSolution.js` to see how to resolve the issue using strict equality.