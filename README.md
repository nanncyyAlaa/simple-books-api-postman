

# Simple Books API – Postman API Automation

This repository contains a **Postman API automation project** for the **Simple Books API**, based on the official documentation by Valentin Despa.
The project demonstrates how to design, automate, and validate REST APIs using Postman with best practices.

---

## 🔗 API Reference

* **Base URL:**

  ```
  https://simple-books-api.click
  ```
* **Official Documentation:**
  [https://github.com/vdespa/introduction-to-postman-course/blob/main/simple-books-api.md](https://github.com/vdespa/introduction-to-postman-course/blob/main/simple-books-api.md)

---

## Project Objectives

* Validate API functionality using automated tests
* Handle authentication using access tokens
* Automate the complete order lifecycle
* Apply Postman automation best practices
* Ensure reliability, correctness, and performance

---

## Automated Endpoints

### Public Endpoints

* `GET /status`
* `GET /books`
* `GET /books/{bookId}`

### Authenticated Endpoints

* `POST /api-clients` (Generate Access Token)
* `POST /orders`
* `GET /orders`
* `GET /orders/{orderId}`
* `PATCH /orders/{orderId}`
* `DELETE /orders/{orderId}`

---

## Authentication Strategy

* Access token is generated using `/api-clients`
* Token is dynamically stored as a **collection variable**
* All secured requests use **Bearer Token Authentication**
* No hardcoded credentials

---

## Automation Scope

* Status code validation
* Response body structure & data type checks
* Query parameter validation (`type`, `limit`)
* Variable chaining between requests
* Error handling validation (404 after delete)
* Data verification after update
* Collection-level performance testing

---

## Performance Testing

* Response time validation

  ```
  Response time < 1000 ms
  ```
* Applied at **collection level** to cover all requests

---

## How to Run

1. Import the Postman Collection
2. Import the Environment (if provided)
3. Open **Postman Runner**
4. Run the collection sequentially

---

## Test Execution Summary

* ✔ Authentication automated
* ✔ Orders lifecycle fully covered
* ✔ No manual steps required
* ✔ Stable and repeatable test execution

---

## Tools Used

* Postman
* JavaScript (Postman Tests)
* REST API

---
