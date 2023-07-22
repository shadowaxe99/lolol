```python
"""
# API Reference

This document provides a detailed explanation of Sara's API, including endpoints, HTTP methods, parameters, request bodies, and example responses.

## Task Management API

### Create Task

**Endpoint:** `/api/tasks/create`
**Method:** `POST`
**Parameters:**
- `title` (string): The title of the task.
- `description` (string): The description of the task.
- `due_date` (string): The due date of the task in the format "YYYY-MM-DD".
- `priority` (string): The priority of the task (e.g., "High", "Medium", "Low").

**Example Request:**
```python
import requests

url = "http://localhost:5000/api/tasks/create"
payload = {
    "title": "Finish project",
    "description": "Complete the documentation and submit the project",
    "due_date": "2022-12-31",
    "priority": "High"
}
response = requests.post(url, json=payload)
print(response.json())
```

**Example Response:**
```json
{
    "status": "success",
    "message": "Task created successfully",
    "task_id": "1234567890"
}
```

### Update Task

**Endpoint:** `/api/tasks/update`
**Method:** `PUT`
**Parameters:**
- `task_id` (string): The ID of the task to update.
- `title` (string): The updated title of the task.
- `description` (string): The updated description of the task.
- `due_date` (string): The updated due date of the task in the format "YYYY-MM-DD".
- `priority` (string): The updated priority of the task (e.g., "High", "Medium", "Low").

**Example Request:**
```python
import requests

url = "http://localhost:5000/api/tasks/update"
payload = {
    "task_id": "1234567890",
    "title": "Finish project",
    "description": "Complete the documentation and submit the project",
    "due_date": "2022-12-31",
    "priority": "High"
}
response = requests.put(url, json=payload)
print(response.json())
```

**Example Response:**
```json
{
    "status": "success",
    "message": "Task updated successfully"
}
```

### Delete Task

**Endpoint:** `/api/tasks/delete`
**Method:** `DELETE`
**Parameters:**
- `task_id` (string): The ID of the task to delete.

**Example Request:**
```python
import requests

url = "http://localhost:5000/api/tasks/delete"
payload = {
    "task_id": "1234567890"
}
response = requests.delete(url, json=payload)
print(response.json())
```

**Example Response:**
```json
{
    "status": "success",
    "message": "Task deleted successfully"
}
```

## Schedule Management API

### Create Appointment

**Endpoint:** `/api/appointments/create`
**Method:** `POST`
**Parameters:**
- `title` (string): The title of the appointment.
- `description` (string): The description of the appointment.
- `start_time` (string): The start time of the appointment in the format "YYYY-MM-DD HH:MM".
- `end_time` (string): The end time of the appointment in the format "YYYY-MM-DD HH:MM".
- `location` (string): The location of the appointment.

**Example Request:**
```python
import requests

url = "http://localhost:5000/api/appointments/create"
payload = {
    "title": "Meeting with client",
    "description": "Discuss project requirements and timeline",
    "start_time": "2022-01-01 09:00",
    "end_time": "2022-01-01 10:00",
    "location": "Office"
}
response = requests.post(url, json=payload)
print(response.json())
```

**Example Response:**
```json
{
    "status": "success",
    "message": "Appointment created successfully",
    "appointment_id": "1234567890"
}
```

### Update Appointment

**Endpoint:** `/api/appointments/update`
**Method:** `PUT`
**Parameters:**
- `appointment_id` (string): The ID of the appointment to update.
- `title` (string): The updated title of the appointment.
- `description` (string): The updated description of the appointment.
- `start_time` (string): The updated start time of the appointment in the format "YYYY-MM-DD HH:MM".
- `end_time` (string): The updated end time of the appointment in the format "YYYY-MM-DD HH:MM".
- `location` (string): The updated location of the appointment.

**Example Request:**
```python
import requests

url = "http://localhost:5000/api/appointments/update"
payload = {
    "appointment_id": "1234567890",
    "title": "Meeting with client",
    "description": "Discuss project requirements and timeline",
    "start_time": "2022-01-01 09:00",
    "end_time": "2022-01-01 10:00",
    "location": "Office"
}
response = requests.put(url, json=payload)
print(response.json())
```

**Example Response:**
```json
{
    "status": "success",
    "message": "Appointment updated successfully"
}
```

### Delete Appointment

**Endpoint:** `/api/appointments/delete`
**Method:** `DELETE`
**Parameters:**
- `appointment_id` (string): The ID of the appointment to delete.

**Example Request:**
```python
import requests

url = "http://localhost:5000/api/appointments/delete"
payload = {
    "appointment_id": "1234567890"
}
response = requests.delete(url, json=payload)
print(response.json())
```

**Example Response:**
```json
{
    "status": "success",
    "message": "Appointment deleted successfully"
}
```

## Email Management API

### Send Email

**Endpoint:** `/api/emails/send`
**Method:** `POST`
**Parameters:**
- `to` (string): The recipient's email address.
- `subject` (string): The subject of the email.
- `body` (string): The body of the email.

**Example Request:**
```python
import requests

url = "http://localhost:5000/api/emails/send"
payload = {
    "to": "example@example.com",
    "subject": "Hello",
    "body": "This is a test email"
}
response = requests.post(url, json=payload)
print(response.json())
```

**Example Response:**
```json
{
    "status": "success",
    "message": "Email sent successfully"
}
```

### Receive Email

**Endpoint:** `/api/emails/receive`
**Method:** `GET`
**Parameters:**
- `limit` (integer): The maximum number of emails to retrieve.

**Example Request:**
```python
import requests

url = "http://localhost:5000/api/emails/receive?limit=10"
response = requests.get(url)
print(response.json())
```

**Example Response:**
```json
{
    "status": "success",
    "message": "Emails retrieved successfully",
    "emails": [
        {
            "id": "1234567890",
            "from": "example@example.com",
            "subject": "Hello",
            "body": "This is a test email"
        },
        {
            "id": "0987654321",
            "from": "another@example.com",
            "subject": "Meeting Reminder",
            "body": "Just a reminder about our meeting tomorrow"
        }
    ]
}
```

## Customization API

### Get User Preferences

**Endpoint:** `/api/customization/preferences`
**Method:** `GET`

**Example Request:**
```python
import requests

url = "http://localhost:5000/api/customization/preferences"
response = requests.get(url)
print(response.json())
```

**Example Response:**
```json
{
    "status": "success",
    "message": "User preferences retrieved successfully",
    "preferences": {
        "reminder_frequency": "daily",
        "email_format": "html",
        "meeting_time": "09:00 AM"
    }
}
```

### Update User Preferences

**Endpoint:** `/api/customization/preferences`
**Method:** `PUT`
**Parameters:**
- `reminder_frequency` (string): The frequency of reminders (e.g., "daily", "weekly", "monthly").
- `email_format` (string): The format of emails (e.g., "plain", "html").
- `meeting_time` (string): The preferred meeting time in the format "HH:MM AM/PM".

**Example Request:**
```python
import requests

url = "http://localhost:5000/api/customization/preferences"
payload = {
    "reminder_frequency": "daily",
    "email_format": "html",
    "meeting_time": "09:00 AM"
}
response = requests.put(url, json=payload)
print(response.json())
```

**Example Response:**
```json
{
    "status": "success",
    "message": "User preferences updated successfully"
}
```

## User Authentication API

### Register User

**Endpoint:** `/api/auth/register`
**Method:** `POST`
**Parameters:**
- `username` (string): The username of the user.
- `password` (string): The password of the user.

**Example Request:**
```python
import requests

url = "http://localhost:5000/api/auth/register"
payload = {
    "username": "example",
    "password": "password123"
}
response = requests.post(url, json=payload)
print(response.json())
```

**Example Response:**
```json
{
    "status": "success",
    "message": "User registered successfully"
}
```

### Login User

**Endpoint:** `/api/auth/login`
**Method:** `POST`
**Parameters:**
- `username` (string): The username of the user.
- `password` (string): The password of the user.

**Example Request:**
```python
import requests

url = "http://localhost:5000/api/auth/login"
payload = {
    "username": "example",
    "password": "password123"
}
response = requests.post(url, json=payload)
print(response.json())
```

**Example Response:**
```json
{
    "status": "success",
    "message": "User logged in successfully",
    "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VyX2lkIjoiMTIzNDU2Nzg5MCIsImlhdCI6MTYzNDU2Nzg5MCwiZXhwIjoxNjM0NTY4NzkwfQ.2XJ0XJ0XJ0XJ0XJ0XJ0XJ0XJ0XJ0XJ0XJ0XJ0XJ0XJ0"
}
```

### Logout User

**Endpoint:** `/api/auth/logout`
**Method:** `POST`

**Example Request:**
```python
import requests

url = "http://localhost:5000/api/auth/logout"
response = requests.post(url)
print(response.json())
```

**Example Response:**
```json
{
    "status": "success",
    "message": "User logged out successfully"
}
```
"""