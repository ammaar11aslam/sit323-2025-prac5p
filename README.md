# SIT323-2025-Prac5P: Enhanced Calculator Microservice

## Overview

This microservice extends the calculator functionality from Task 4.1P by adding advanced arithmetic operations:

- Exponentiation
- Square Root
- Modulo

It also includes improved error handling for invalid input scenarios and has now been fully Dockerised for consistent local development and deployment.

---

## Dockerised Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/ammaar11aslam/sit323-2025-prac5p
cd sit323-2025-prac4c
```

### 2. Run the App with Docker Compose

```bash
docker-compose up --build
```

The app will be available at:

```
http://localhost:3000
```

> Ensure Docker Desktop is running before executing the above command.

---

## 🧾 API Endpoints

### Basic Operations

- `GET /add?num1=10&num2=5`
- `GET /subtract?num1=10&num2=5`
- `GET /multiply?num1=10&num2=5`
- `GET /divide?num1=10&num2=5`

### Advanced Operations

- `GET /exponent?base=2&power=3`
- `GET /sqrt?num=16`
- `GET /modulo?num1=10&num2=3`

---

## Error Handling

- Invalid numbers:
  ```json
  { "error": "Both num1 and num2 must be valid numbers." }
  ```
- Division or modulo by zero:
  ```json
  { "error": "Division by zero is not allowed." }
  ```
- Square root of negative number:
  ```json
  { "error": "Square root of negative number is not supported." }
  ```

---

## 🔍 How to Test This App

### 1. **Browser**

Paste API links into the address bar, e.g.  
[http://localhost:3000/sqrt?num=16](http://localhost:3000/sqrt?num=16)

### 2. **Postman or Thunder Client**

Make structured GET requests with query parameters.

### 3. **Command Line (cURL)**

Example:

```bash
curl "http://localhost:3000/exponent?base=2&power=4"
```

---

## Project Structure

```
sit323-2025-prac4c/
├── Dockerfile
├── docker-compose.yml
├── server.js
├── package.json
└── README.md
```

---

## Tools Used

- Node.js
- Express
- Docker & Docker Compose
- Visual Studio Code
- GitHub

---

## Notes

If you encounter image pull issues with Docker, consider using a custom Dockerfile that installs Node.js from alternative sources or builds it manually, as included in this project.
