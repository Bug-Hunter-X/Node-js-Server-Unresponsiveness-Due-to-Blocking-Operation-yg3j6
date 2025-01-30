# Node.js Server Unresponsiveness

This repository demonstrates a common issue in Node.js where a long-running operation in the request handler can cause the server to hang or become unresponsive.  The `server.js` file shows the problematic code, while `serverSolution.js` provides a solution using asynchronous operations.

## Problem

The problem arises when a synchronous operation takes a significant amount of time to complete within the request handler. Node.js is single-threaded, and this blocking operation prevents the server from processing other requests. This can lead to poor performance or a complete unresponsive server.

## Solution

The solution uses asynchronous operations. Node.js's event loop can handle concurrent requests efficiently when operations are non-blocking.  In this example, we simulate this via asynchronous code.