# Unhandled Asynchronous Errors in Node.js Express Server

This repository demonstrates a common error in Node.js asynchronous programming: unhandled errors within asynchronous callbacks.  The provided `bug.js` file showcases an Express server that can crash due to an unhandled error in a `setTimeout` callback.  The `bugSolution.js` file provides a solution using error handling to prevent the server crash.

## Bug Description:

The server simulates an asynchronous operation. Half the time it works fine.  Half the time, it throws an error, causing the entire server to crash without proper error handling.

## Solution:

The solution involves wrapping the asynchronous operation in a `try...catch` block within the callback to handle potential errors gracefully.  This prevents the server crash and allows for logging or other error handling mechanisms.

## How to Run:

1. Clone this repository.
2. Navigate to the directory.
3. Run `node bug.js` to see the unhandled error and server crash.
4. Run `node bugSolution.js` to see the solution in action.