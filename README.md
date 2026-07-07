# API Testing — JSONPlaceholder REST API
Manual QA project testing the JSONPlaceholder REST API using Postman, covering GET, POST, PUT, PATCH, and DELETE requests across Users, Posts, and Comments resources.

## Objective
Practice manual API testing fundamentals — writing test cases, executing requests, validating responses, and documenting bugs — using a public REST API.

## Tools Used
- **Postman** — sending requests and inspecting responses
- **JSONPlaceholder API** — public fake REST API for testing (https://jsonplaceholder.typicode.com)
- **Excel / Google Sheets** — test case documentation and bug reporting

## Scope
20 test cases covering:
- GET requests (Users, Posts, Comments — including single record, invalid ID, and query parameter filtering)
- POST requests (creating a new post/user)
- PUT and PATCH requests (full and partial updates)
- DELETE requests
- Positive tests (valid input) and negative tests (invalid ID, empty body, missing required field, wrong data type)
- Response validation (status codes, headers, expected fields)

## Files in this Repo
- `API Testing — JSONPlaceholder REST API.xlsx` — contains two sheets: **Test Case Template** (20 test cases with steps, expected result, actual result, and pass/fail status) and **Bug Report Template** (3 documented bugs found during testing)
- `JSONPlaceholder API Tests.postman_collection.json` — exported Postman collection with all requests used

## Summary of Results
- **20 test cases executed**
- **17 Passed**, **3 Failed**
- **3 bugs found:**
  - `POST /posts` accepts an empty body and still returns 201 Created instead of a validation error
  - `POST /users` accepts a numeric value for the email field instead of rejecting it
  - `POST /posts` accepts a request missing the required title field
  
  (see Bug Report Template for full details)

## Key Learnings
- How to write clear, structured test cases with expected vs actual results
- Difference between positive and negative testing
- How to identify and document real API bugs with reproducible steps
- Basics of REST API status codes (200, 201, 404) and when each should apply
- CRUD operations across an API (Create, Read, Update, Delete)
- Validating response headers and query parameter filtering

## Note
JSONPlaceholder is a free, fake REST API used for testing and prototyping purposes only. It does not represent a real, production application, and no data returned by it is actually saved or persisted on any server. This project was built as part of a self-directed QA learning plan and serves as a foundational, beginner-level exercise to practice manual API testing concepts — including writing test cases, executing requests, and reporting bugs — before applying these skills to real-world applications.
