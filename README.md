# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: the lack of proper error handling for invalid or unexpected input. Specifically, the example shows a route that retrieves a user by ID.  If the ID is not a valid number, the code will throw an error.

The `bug.js` file contains the erroneous code. The `bugSolution.js` file provides a corrected version with comprehensive error handling.

## Bug

The bug lies in the absence of input validation and error handling.  The code attempts to parse the `userId` as an integer without checking if it's a valid integer. If a non-numeric `userId` is passed, `parseInt` will return `NaN`, leading to a failed search and, potentially, an unhandled exception or unexpected behavior. 

## Solution

The solution includes thorough input validation. It checks if `userId` can be parsed as an integer and handles the case where no user is found with the given ID.