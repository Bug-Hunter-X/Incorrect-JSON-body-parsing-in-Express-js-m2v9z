# Incorrect JSON Body Parsing in Express.js
This repository demonstrates a common error in Express.js applications where the JSON request body is not parsed correctly, leading to unexpected behavior. The issue stems from incorrect use or absence of body-parsing middleware.

## Bug Description
The provided Express.js code attempts to handle POST requests to the '/user' route.  It intends to read the JSON payload from the request body and log it to the console. However, due to a missing or incorrectly configured body-parser, `req.body` remains empty, causing the application to fail silently or produce unexpected results.

## Bug Solution
The solution involves ensuring that the appropriate body-parsing middleware (`express.json()`) is correctly integrated into the Express app before defining routes that expect a JSON payload.