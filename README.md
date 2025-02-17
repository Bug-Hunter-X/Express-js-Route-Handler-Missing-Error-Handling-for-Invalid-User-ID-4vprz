# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input.  Specifically, the provided code lacks proper handling for cases where a user ID is not a valid integer.

## Bug

The `bug.js` file contains the buggy code.  The route handler attempts to parse the user ID as an integer but doesn't check if the parsing was successful. If the ID is not an integer, this will cause an error.

## Solution

The `bugSolution.js` file provides a corrected version of the code.  It includes explicit error handling to check if the user ID is a valid number and to gracefully handle cases where it's not.

## How to Run

1. Clone this repository.
2. Navigate to the repository directory.
3. Run `npm install express` to install the necessary dependency.
4. Run `node bug.js` to see the buggy behavior.  You'll need to run a test call with an invalid user id e.g. `/users/abc`
5. Run `node bugSolution.js` to see the corrected behavior.