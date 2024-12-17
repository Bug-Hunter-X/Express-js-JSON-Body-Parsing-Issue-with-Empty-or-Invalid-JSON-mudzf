# Express.js JSON Body Parsing Issue

This repository demonstrates a common issue encountered when using Express.js to parse JSON data from POST requests. The problem arises when the request body is either empty or contains invalid JSON data.  The server fails to handle these cases correctly.

## Bug Description

The provided `bug.js` file shows an Express.js server that attempts to parse JSON data from POST requests to `/data`. When an empty or invalid JSON is sent, the server throws an error or fails to process the request, leading to unexpected behavior.  This can occur due to a missing or incorrect `Content-Type` header in the client request, or due to malformed JSON being sent.

## Solution

The `bugSolution.js` file provides a solution that addresses this issue by using middleware to gracefully handle empty or invalid JSON requests. This solution checks for empty request bodies and parses valid JSON bodies, sending appropriate error responses for any errors. 