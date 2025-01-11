# Node.js Server Hang Issue

This repository demonstrates a common issue in Node.js servers where a long-running operation (simulated here with `setTimeout`) blocks the event loop, causing the server to hang and not respond to requests for an extended period.

## Problem

The `server.js` file contains a simple Express.js server that introduces a 5-second delay before sending a response.  During this 5 seconds, the server is unresponsive to any new requests.

## Solution

The `serverSolution.js` file demonstrates how to address this problem by using asynchronous techniques like promises and async/await. This prevents the event loop from being blocked.

## How to reproduce

1. Clone this repository.
2. Run `npm install` to install Express.js.
3. Run `node server.js`. Send a request to the server (e.g. using a browser). Observe the delay.
4. Run `node serverSolution.js`. Send a request to the server. Observe the improved responsiveness.