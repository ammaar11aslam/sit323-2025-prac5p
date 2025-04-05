# SIT323-2025-Prac4C: Enhanced Calculator Microservice

## Overview

This microservice extends the calculator functionality from Task 4.1P by adding advanced arithmetic operations:

- Exponentiation
- Square Root
- Modulo

It also retains and improves error handling to deliver more informative responses for invalid input scenarios.

## Setup Instructions

### 1. Clone the Repository

git clone https://github.com/ammaar11aslam/sit323-2025-prac4c
cd sit323-2025-prac4c

### 2. Install Dependencies

npm install

### 3. Run the Server

node server.js

### 4. Access the API

Base URL: `http://localhost:3000`

## API Endpoints

### ✅ Basic Operations

- `GET /add?num1=10&num2=5`
- `GET /subtract?num1=10&num2=5`
- `GET /multiply?num1=10&num2=5`
- `GET /divide?num1=10&num2=5`

### ✅ Advanced Operations

- `GET /exponent?base=2&power=3`
- `GET /sqrt?num=16`
- `GET /modulo?num1=10&num2=3`

## Error Handling

- Invalid numbers: returns `{ "error": "Both num1 and num2 must be valid numbers." }`
- Division or modulo by zero: returns `{ "error": "Division by zero is not allowed." }`
- Square root of negative number: returns `{ "error": "Square root of negative number is not supported." }`

## How to Conveniently Use This App

### 1. **Browser**

Great for quick tests using only `GET` endpoints. Paste the URL with parameters directly into the address bar.

### 2. **Frontend Integration**

You can build a simple HTML+JS frontend to call these endpoints using `fetch` or `axios`.

### 3. **Shell / CLI with curl**

Example:

curl "http://localhost:3000/exponent?base=2&power=4"

## Tools Used

- Node.js
- Express
- Visual Studio Code
- GitHub
