# Node.js Server Blocking Example

This repository demonstrates a common issue in Node.js applications: blocking the event loop with a long-running synchronous operation.  The server.js file contains a simple HTTP server with a computationally intensive loop in the request handler. This causes the server to freeze and become unresponsive to new requests.  The solution, provided in serverSolution.js, illustrates how to address this using asynchronous techniques.

## How to Reproduce

1. Clone the repository.
2. Navigate to the directory.
3. Run `node server.js`.
4. Open a browser and navigate to `http://localhost:3000/`.
5. Observe that the server responds but becomes unresponsive to further requests until the loop completes.

## Solution

The solution uses asynchronous techniques (as demonstrated in serverSolution.js) to prevent the main event loop from blocking.