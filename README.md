# Express.js Route Handler Missing Error Handling

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input.

The `bug.js` file shows the erroneous code.  The `bugSolution.js` file provides a corrected version.

## Bug Description

The `/users/:id` route attempts to retrieve a user based on their ID.  It parses the ID as an integer but doesn't handle cases where the ID is not an integer or doesn't exist in the `users` array. This will lead to unexpected errors or crashes.

## Solution

The solution adds robust error handling: checking if the `userId` is a valid number and handling the case where the user isn't found.