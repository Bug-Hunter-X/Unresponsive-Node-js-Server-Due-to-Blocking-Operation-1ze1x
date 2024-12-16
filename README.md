# Unresponsive Node.js Server Due to Blocking Operation

This repository demonstrates a common issue in Node.js where a long-running synchronous operation in a request handler blocks the event loop, making the server unresponsive.  The `blocking-server.js` file shows the problematic code, while `unblocking-server.js` provides a solution using asynchronous operations.

## Problem

Node.js is single-threaded, meaning all code runs in a single thread. A long-running synchronous operation in a request handler will block the event loop, preventing the server from handling any other requests until the operation completes.

## Solution

The solution is to use asynchronous operations instead of synchronous ones. This allows the event loop to continue processing other requests while the long-running task is performed in the background.