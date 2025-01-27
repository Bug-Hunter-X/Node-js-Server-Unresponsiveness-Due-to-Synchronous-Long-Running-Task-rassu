# Node.js Server Unresponsiveness
This repository demonstrates a common issue in Node.js where a long-running synchronous operation in a request handler can cause the server to hang or become unresponsive.  The `server.js` file contains the buggy code, while `serverSolution.js` provides a corrected version using asynchronous operations.

## Problem
Node.js is single-threaded and relies on the event loop to handle multiple requests concurrently.  A long-running synchronous operation blocks the event loop, preventing it from processing other events. This leads to the server becoming unresponsive.

## Solution
The solution is to refactor long-running tasks to use asynchronous operations, allowing the event loop to continue processing other requests. Asynchronous functions do not block the main thread.  This is achieved using techniques like promises, async/await, or callbacks.