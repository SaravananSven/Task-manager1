<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

<p align="center">
<a href="https://github.com/laravel/framework/actions"><img src="https://github.com/laravel/framework/workflows/tests/badge.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

# Laravel Task Management API 🚀

A simple Task Management API built with Laravel that allows users to create, update, delete, and list tasks.

## 📌 Features
✅ Create, update, and delete tasks  
✅ List all tasks with pagination  
✅ Request validation for input data  
✅ RESTful API with JSON responses  

## 🛠 Setup Instructions

### 1️⃣ Clone the repository
```php
git clone https://github.com/SaravananSven/Task-manager1.git
cd Task-manager
```

### 2️⃣ Install dependencies
```php
composer create-project --prefer-dist laravel/laravel
```
### 3️⃣ Set up environment variables
```php
cp .env.example .env
DB_DATABASE=your_database_name
DB_USERNAME=your_database_user
DB_PASSWORD=your_database_password
```

### 4️⃣ Generate application key
```php
php artisan key:generate
```

### 5️⃣ Run database migrations
```php
php artisan migrate
```

### 6️⃣ Start the Laravel server
```php
php artisan serve
```
Your API will now be running at:
http://127.0.0.1:8000/api/tasks


### 🔗 API Endpoints & Usage
## 📌 Create a Task
Method: POST
Endpoint: /api/tasks
Request Body (JSON):
```php
{
  "title": "Wake up at 6",
  "description": "Finish the given task before the deadline",
  "status": "pending",
  "due_date": "2025-03-05"
}
```

### 📌 Get All Tasks
## Method: GET
Endpoint: /api/tasks
Response Example:
```php
[
  {
    "id": 1,
    "title": "Wake up at 6",
    "description": "Finish the given task before the deadline",
    "status": "pending",
    "due_date": "2025-03-05"
  },
  {
    "id": 2,
    "title": "Prepare for interview",
    "description": "Review Laravel concepts",
    "status": "completed",
    "due_date": "2025-03-06"
  }
]
```
### 📌 Get a Single Task
## Method: GET
Endpoint: /api/tasks/{id}
Example Request: /api/tasks/1
Response Example:
```php
{
  "id": 1,
  "title": "Complete Laravel API",
  "description": "Finish the given task before the deadline",
  "status": "pending",
  "due_date": "2025-03-05"
}
```
### 📌 Update a Task
##  Method: PUT
Endpoint: /api/tasks/{id}
Example Request: /api/tasks/1
Request Body (JSON):
```
{
  "title": "Updated Task",
  "status": "completed"
}
```
### 📌 Delete a Task
## Method: DELETE
Endpoint: /api/tasks/{id}
Example Request: /api/tasks/1
Response:
```
{
  "message": "Task deleted successfully"
}
```
### 🎯 Additional Features
✅ Laravel RESTful API design
✅ Uses Laravel’s Eloquent ORM for database operations
✅ Form request validation to ensure correct data
✅ Proper error handling for missing tasks
✅ Structured JSON responses

### 🛠 Technologies Used
1.Laravel (PHP Framework)
2.MySQL (Database)
3.Postman (API Testing)
4.Eloquent ORM (Database Handling)

### 📌 How to Test the API in Postman
1.Open Postman.
2.Enter the API endpoint (http://127.0.0.1:8000/api/tasks).
3.Choose the correct HTTP method (GET, POST, PUT, DELETE).
4.If sending data (POST/PUT), go to the Body tab and select raw → JSON.
5.Click Send to see the response.
