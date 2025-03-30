
# Calculator Microservice

## Overview

This project implements a basic calculator microservice using Node.js and Express. The microservice exposes several API endpoints that allow users to perform basic arithmetic operations (addition, subtraction, multiplication, and division) along with error handling for invalid inputs and division by zero.

### Features
- Basic arithmetic operations (addition, subtraction, multiplication, division)
- Error handling for invalid inputs and division by zero
- API responses in JSON format

## Getting Started

Follow the steps below to set up and run the project locally.

### Prerequisites

- [Node.js](https://nodejs.org/en/download/) installed on your machine
- A text editor (such as [Visual Studio Code](https://code.visualstudio.com/)) for editing files

### Installing

1. Clone the repository to your local machine:
   ```bash
   git clone https://github.com/your-username/sit323-2025-prac4c.git
   ```

2. Navigate into the project folder:
   ```bash
   cd sit323-2025-prac4c
   ```

3. Install the required dependencies:
   ```bash
   npm install
   ```

### Running the Server

1. To start the server, run the following command:
   ```bash
   node server.js
   ```

2. The server will start and be available at `http://localhost:3000`.

### Using the API

The API exposes the following endpoints:

#### 1. Addition
- **Endpoint**: `/add`
- **Method**: `GET`
- **Parameters**: `num1`, `num2` (both should be numbers)
- **Example**:
  ```bash
  http://localhost:3000/add?num1=5&num2=3
  ```
- **Response**:
  ```json
  { "result": 8 }
  ```

#### 2. Subtraction
- **Endpoint**: `/subtract`
- **Method**: `GET`
- **Parameters**: `num1`, `num2` (both should be numbers)
- **Example**:
  ```bash
  http://localhost:3000/subtract?num1=5&num2=3
  ```
- **Response**:
  ```json
  { "result": 2 }
  ```

#### 3. Multiplication
- **Endpoint**: `/multiply`
- **Method**: `GET`
- **Parameters**: `num1`, `num2` (both should be numbers)
- **Example**:
  ```bash
  http://localhost:3000/multiply?num1=5&num2=3
  ```
- **Response**:
  ```json
  { "result": 15 }
  ```

#### 4. Division
- **Endpoint**: `/divide`
- **Method**: `GET`
- **Parameters**: `num1`, `num2` (both should be numbers)
- **Example**:
  ```bash
  http://localhost:3000/divide?num1=6&num2=3
  ```
- **Response**:
  ```json
  { "result": 2 }
  ```

- **Error Handling**:
  - If invalid parameters are passed (non-numeric values), the response will return a `400` error with a message:
    ```json
    { "error": "Invalid input parameters" }
    ```
  - If attempting to divide by zero, the response will return a `400` error with the message:
    ```json
    { "error": "Cannot divide by zero" }
    ```

### Example Client Usage

In the `index.js` file, the client communicates with the server by sending requests to the API. You can modify the `operation` argument and the numbers to test the calculator operations.

```javascript
performOperation('add', 5, 3);  // Change the operation to 'subtract', 'multiply', or 'divide' as needed
```

This script will fetch the result from the API and log the output to the console.

### Error Handling

The microservice has been designed to handle the following errors:

- **Invalid input**: If non-numeric values are passed for `num1` or `num2`, the server responds with an error message indicating invalid input.
- **Division by zero**: If `num2` is `0` during a division operation, the server responds with an error message indicating that division by zero is not allowed.



