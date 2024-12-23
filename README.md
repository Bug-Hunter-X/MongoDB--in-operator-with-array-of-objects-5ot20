# MongoDB $in operator with array of objects

This repository demonstrates a common error when using the `$in` operator in MongoDB queries with an array of objects.  The issue arises when attempting to match documents where a field's value is an object within a given set of objects. The naive approach fails to produce the intended results.

The `bug.js` file illustrates the problematic query, while `bugSolution.js` provides a corrected version using the `$or` operator to achieve the desired outcome.

## Setup

1. Ensure you have MongoDB installed and running.
2. Create a MongoDB collection and populate it with sample documents.
3. Run the JavaScript files (bug.js and bugSolution.js) using the mongo shell.

## Solution
The solution involves restructuring the query to utilize the `$or` operator, allowing for individual object comparisons to correctly identify matching documents.