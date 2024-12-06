# Unhandled Promise Rejection in Express.js Async Route

This repository demonstrates a common error in Express.js applications: unhandled promise rejections in asynchronous route handlers.  The `bug.js` file showcases the problematic code, where an asynchronous operation is performed without proper error handling.  The `bugSolution.js` file provides a corrected version with comprehensive error handling.

## Bug Description

The `bug.js` example uses a `Promise` within a route handler. If the asynchronous operation (`someAsyncOperation`) fails, the error is not caught, resulting in an unhandled promise rejection.  This can lead to application instability or crashes, especially in production environments.

## Solution

The `bugSolution.js` demonstrates the proper way to handle errors in asynchronous route handlers.  Using `.catch()` ensures that any errors thrown by the asynchronous operation are gracefully handled and don't lead to unhandled rejections.

## How to reproduce

1. Clone the repository.
2. Navigate to the project directory.
3. Run `npm install` to install Express.js.
4. Run `node bug.js` to execute the buggy code. Observe the unhandled promise rejection in the console.
5. Run `node bugSolution.js` to execute the corrected code. Observe that errors are now handled gracefully.