# Unhandled Promise Rejection in Node.js

This repository demonstrates a common error in Node.js applications: unhandled promise rejections.  Unhandled rejections can lead to crashes or unexpected behavior without clear error messages.

## The Problem

The `bug.js` file contains code that intentionally creates an unhandled promise rejection.  Running this code will not produce an immediate error, but it will result in a silent crash or unpredictable behavior later in the application's lifecycle, depending on your Node.js version and environment.

## The Solution

The `bugSolution.js` file demonstrates the correct way to handle promise rejections using the `process.on('unhandledRejection', ...)` event listener.  This listener provides a mechanism to gracefully handle and log these rejections, preventing silent failures. 

## How to Run

1. Clone this repository.
2. Navigate to the directory.
3. Run `node bug.js` (to observe the unhandled rejection). 
4. Run `node bugSolution.js` (to see the proper handling of the rejection).

## Conclusion

Always handle promise rejections to ensure the stability and reliability of your Node.js applications.