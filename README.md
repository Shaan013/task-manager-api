
# Student Record System API

## 1. Introduction

The **Student Record System API** is a backend solution designed to manage student information effectively. Built with **Node.js** and **Express.js**, this API facilitates essential operations such as:

- Adding new students
- Retrieving all or individual student records
- Updating student details
- Deleting records
- Searching students by name or course

This project showcases the implementation of a practical and minimal RESTful API for data management using in-memory storage.

---

## 2. Key Features

The API provides comprehensive functionalities for managing student records:

- **Add Student:** Register new students with name, unique roll number, and course.
- **View All Students:** Get a list of all registered students.
- **View Student by Roll Number:** Retrieve a student’s record using their roll number.
- **Update Student Record:** Modify a student’s name or course.
- **Delete Student Record:** Remove a student from the system using roll number.
- **Search Students:** Find students using partial matches on name or course via query parameters.

---

## 3. Technologies Used

- **Node.js**: JavaScript runtime environment for backend development.
- **Express.js**: Web framework for building RESTful APIs with Node.js.
- **In-Memory Data Storage**: JavaScript array is used to temporarily store student records.

> *Note: For production use, consider integrating a database like MongoDB, PostgreSQL, or lowdb for persistent storage.*

---

## 4. API Endpoints Overview

**Base URL:** `http://localhost:3002`

| Method | Endpoint               | Description |
|--------|------------------------|-------------|
| POST   | `/students`            | Create a new student record. |
| GET    | `/students`            | Get all students (supports search via `?name=value` or `?course=value`). |
| GET    | `/students/:rollNo`    | Get student by roll number. |
| PUT    | `/students/:rollNo`    | Update student details. |
| DELETE | `/students/:rollNo`    | Delete student record. |

### Request Examples:

#### POST `/students`
```json
{
  "name": "John Doe",
  "rollNo": "105",
  "course": "Mathematics"
}
````

#### GET `/students?course=Mathematics`

Search students by course.

#### PUT `/students/105`

```json
{
  "name": "John Smith",
  "course": "Physics"
}
```

---

## 5. Setup and How to Run

Follow the steps below to run the API locally:

### Step 1: Create Project Directory

```bash
mkdir student-record-api
cd student-record-api
```

### Step 2: Initialize Node.js Project

```bash
npm init -y
```

### Step 3: Install Express.js

```bash
npm install express
```

### Step 4: Create `server.js`

Create a file named `server.js` in the project root and paste the API implementation code into it.

### Step 5: Run the Server

```bash
node server.js
```

Your API will be live at `http://localhost:3002`.

---

## 6. Testing the API

You can use **Postman** or any other API testing tool to test the endpoints:

* Set the appropriate HTTP method (GET, POST, PUT, DELETE).
* Use the correct URL (`http://localhost:3002/...`).
* For POST and PUT, set `Content-Type` to `application/json` and provide the JSON body.
* Observe the response status codes and returned JSON data.

---

## Created By

**Shaan**

---


