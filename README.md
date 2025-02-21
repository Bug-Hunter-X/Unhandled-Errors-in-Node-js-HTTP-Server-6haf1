# Unhandled Errors in Node.js HTTP Server

This repository demonstrates a common error in Node.js: missing error handling in an HTTP server request listener.  The initial `bug.js` file lacks proper error handling, while `bugSolution.js` provides a corrected version.

## Problem

The original code creates a simple HTTP server but fails to handle potential errors during request processing.  If an error occurs (e.g., database connection failure, file system error), the server will likely crash without providing informative error messages.

## Solution

The solution includes a `try...catch` block within the request listener to gracefully handle errors.  Error details are logged to the console, and a custom error response is sent to the client.  This prevents server crashes and provides more robust error management.

## Usage

1. Clone this repository.
2. Run `node bug.js` to see the unhandled error behavior.
3. Run `node bugSolution.js` to see the improved error handling.