# CareerPASS API Documentation

Welcome to the CareerPASS API documentation. This API provides endpoints for managing users, administering assessments, handling assessment submissions, and more.

## Table of Contents

- [Endpoints](#endpoints)
- [Authentication](#authentication)
- [Responses](#responses)
- [Error Handling](#error-handling)

## Endpoints

### Users

- **POST /register**
  - Description: Register a new user.
- **GET /adminLogin**
  - Description: Admin login.
- **GET /showApplicants**
  - Description: Retrieve all applicants.
- **POST /adminRegister**
  - Description: Register a new admin.

### Question Management - CRUD

- **Create Question**
  - Endpoint: baseURL/createQuestion
  - Method: POST
  - Description: Create a new assessment question.

- **Get All Questions**
  - Endpoint: baseURL/getAllQuestions
  - Method: GET
  - Description: Retrieve all assessment questions.

- **Update Question**
  - Endpoint: baseURL/updateQuestion/questionId
  - Method: PUT
  - Description: Update an existing assessment question.

- **Delete Question**
  - Endpoint: baseURL/deleteQuestion/questionId
  - Method: DELETE
  - Description: Delete an existing assessment question.

- **Get Questions By Id**
  - Endpoint: baseURL/getQuestionById/questionId
  - Method: GET
  - Description: Retrieves a specific assessment question.

### Assessment Submission

- **Submit Assessment**
  - Endpoint: baseURL/submit
  - Method: POST
  - Description: Submit assessment responses.

### Scoring and Recommendations

- **Calculate Math and Logic Scores and Recommendations for Section 1 (Cognitive Abilities)**
  - Endpoint: baseURL/math-logic-scores-recommendation
  - Method: POST
  - Description: Calculate scores and recommend learning tracks based on assessment results for mathematical aptitude and logical reasoning.

- **Calculate Scores and Recommendations for Sections 2-5**
  - Endpoint: baseURL/scores-recommendations
  - Method: POST
  - Description: Calculate scores and recommend learning tracks based on assessment results for personality traits.

### Contact Form Submission

- **Form Submission**
  - Endpoint: baseURL/contactUs
  - Method: POST
  - Description: Submits applicants' inquiries.

- **Show Applicants Queries**
  - Endpoint: baseURL/getAllSubmissions
  - Method: GET
  - Description: Retrieve a list of all applicant's queries.

## Authentication

Authentication is required for certain endpoints, such as creating assessment questions or submitting assessments. Authentication is implemented using JSON Web Tokens (JWT). Users must include their JWT token in the Authorization header of the request.

## Responses

The API returns responses in JSON format. Successful responses include a 200 OK status code, while error responses include appropriate status codes (e.g., 400 Bad Request, 401 Unauthorized, 500 Internal Server Error) along with an error message.

## Error Handling

The API includes error handling to ensure that errors are appropriately handled and returned to the client. Errors are returned in JSON format with an error message describing the issue.
