# API Testing — JSONPlaceholder REST API

Manual QA project testing the JSONPlaceholder REST API using Postman, covering GET and POST requests across Users, Posts, and Comments resources.

## Objective
Practice manual API testing fundamentals — writing test cases, executing requests, validating responses, and documenting bugs — using a public REST API.

## Tools Used
- **Postman** — sending requests and inspecting responses
- **JSONPlaceholder API** — public fake REST API for testing (https://jsonplaceholder.typicode.com)
- **Excel / Google Sheets** — test case documentation and bug reporting

## Scope
10 test cases covering:
- GET requests (Users, Posts, Comments)
- POST requests (creating a new post)
- Positive tests (valid input) and negative tests (invalid ID, empty body)
- Response validation (status codes, expected fields)

## Files in this Repo
- `Test_Case_Template.xlsx` — 10 test cases with steps, expected result, actual result, and pass/fail status
- `Bug_Report_Template.xlsx` — documented bug found during testing
- `JSONPlaceholder_API_Tests.postman_collection.json` — exported Postman collection with all requests used

## Summary of Results
- **10 test cases executed**
- **9 Passed**, **1 Failed**
- **1 bug found:** POST /posts accepts an empty body and still returns 201 Created instead of a validation error (see Bug Report for details)

## Key Learnings
- How to write clear, structured test cases with expected vs actual results
- Difference between positive and negative testing
- How to identify and document a real API bug with reproducible steps
- Basics of REST API status codes (200, 201, 404) and when each should apply

## Note
JSONPlaceholder is a free, fake REST API used for testing and prototyping purposes only. It does not represent a real, production application, and no data returned by it is actually saved or persisted on any server. This project was built as part of a self-directed QA learning plan and serves as a foundational, beginner-level exercise to practice manual API testing concepts — including writing test cases, executing requests, and reporting bugs — before applying these skills to real-world applications.
