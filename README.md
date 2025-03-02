
</p># Task-manager1
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
cd Task-manager1
```

### 2️⃣ Install dependencies
```php
composer install
```
### 3️⃣ Set up environment variables
change the .env.example to .env
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
## 🎯 Additional Features
✅ Laravel RESTful API design
✅ Uses Laravel’s Eloquent ORM for database operations
✅ Form request validation to ensure correct data
✅ Proper error handling for missing tasks
✅ Structured JSON responses

## 🛠 Technologies Used
1.Laravel (PHP Framework)
2.MySQL (Database)
3.Postman (API Testing)
4.Eloquent ORM (Database Handling)

## 📌 How to Test the API in Postman
1.Open Postman.
2.Enter the API endpoint (http://127.0.0.1:8000/api/tasks).
3.Choose the correct HTTP method (GET, POST, PUT, DELETE).
4.If sending data (POST/PUT), go to the Body tab and select raw → JSON.
5.Click Send to see the response.
## About Laravel

Laravel is a web application framework with expressive, elegant syntax. We believe development must be an enjoyable and creative experience to be truly fulfilling. Laravel takes the pain out of development by easing common tasks used in many web projects, such as:

- [Simple, fast routing engine](https://laravel.com/docs/routing).
- [Powerful dependency injection container](https://laravel.com/docs/container).
- Multiple back-ends for [session](https://laravel.com/docs/session) and [cache](https://laravel.com/docs/cache) storage.
- Expressive, intuitive [database ORM](https://laravel.com/docs/eloquent).
- Database agnostic [schema migrations](https://laravel.com/docs/migrations).
- [Robust background job processing](https://laravel.com/docs/queues).
- [Real-time event broadcasting](https://laravel.com/docs/broadcasting).

Laravel is accessible, powerful, and provides tools required for large, robust applications.

## Learning Laravel

Laravel has the most extensive and thorough [documentation](https://laravel.com/docs) and video tutorial library of all modern web application frameworks, making it a breeze to get started with the framework.

You may also try the [Laravel Bootcamp](https://bootcamp.laravel.com), where you will be guided through building a modern Laravel application from scratch.

If you don't feel like reading, [Laracasts](https://laracasts.com) can help. Laracasts contains thousands of video tutorials on a range of topics including Laravel, modern PHP, unit testing, and JavaScript. Boost your skills by digging into our comprehensive video library.

## Laravel Sponsors

We would like to extend our thanks to the following sponsors for funding Laravel development. If you are interested in becoming a sponsor, please visit the [Laravel Partners program](https://partners.laravel.com).

### Premium Partners

- **[Vehikl](https://vehikl.com/)**
- **[Tighten Co.](https://tighten.co)**
- **[WebReinvent](https://webreinvent.com/)**
- **[Kirschbaum Development Group](https://kirschbaumdevelopment.com)**
- **[64 Robots](https://64robots.com)**
- **[Curotec](https://www.curotec.com/services/technologies/laravel/)**
- **[Cyber-Duck](https://cyber-duck.co.uk)**
- **[DevSquad](https://devsquad.com/hire-laravel-developers)**
- **[Jump24](https://jump24.co.uk)**
- **[Redberry](https://redberry.international/laravel/)**
- **[Active Logic](https://activelogic.com)**
- **[byte5](https://byte5.de)**
- **[OP.GG](https://op.gg)**

## Contributing

Thank you for considering contributing to the Laravel framework! The contribution guide can be found in the [Laravel documentation](https://laravel.com/docs/contributions).

## Code of Conduct

In order to ensure that the Laravel community is welcoming to all, please review and abide by the [Code of Conduct](https://laravel.com/docs/contributions#code-of-conduct).

## Security Vulnerabilities

If you discover a security vulnerability within Laravel, please send an e-mail to Taylor Otwell via [taylor@laravel.com](mailto:taylor@laravel.com). All security vulnerabilities will be promptly addressed.

## License

The Laravel framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
