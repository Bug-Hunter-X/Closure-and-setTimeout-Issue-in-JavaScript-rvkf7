# Closure and setTimeout Issue in JavaScript

This repository demonstrates a common issue in JavaScript involving closures and the `setTimeout` function.  The problem arises from how closures capture variables in loops. 

The `bug.js` file contains code that intends to log the numbers 0 through 9 with a one-second delay between each log. However, due to the asynchronous nature of `setTimeout` and the way closures work, it will instead log the value '10' ten times.

The solution, provided in `bugSolution.js`, addresses this by using an immediately invoked function expression (IIFE) to create a new scope for each iteration of the loop, ensuring each closure captures its own value of `i`.

This example highlights an important concept in JavaScript programming and provides a clear solution to a frequently encountered problem.