# Library-Management-System
// README.md
/*
# Library Management System

## Overview
A simple ASP.NET Core Library Management System with full CRUD operations.

## Features
- Book management (Create, Read, Update, Delete)
- SQL Server database integration with Entity Framework Core
- RESTful API endpoints

## Setup Instructions
### Prerequisites
- .NET 6 SDK or later
- SQL Server

### Installation
1. Clone this repository:
   ```
   git clone https://github.com/yourusername/library-management-system.git
   cd library-management-system
   ```
2. Update the database connection string in `appsettings.json`.
3. Run migrations and update the database:
   ```
   dotnet ef migrations add InitialCreate
   dotnet ef database update
   ```
4. Start the application:
   ```
   dotnet run
   ```

## API Endpoints
- `GET /api/books` - Get all books
- `GET /api/books/{id}` - Get book by ID
- `POST /api/books` - Add new book
- `PUT /api/books/{id}` - Update book
- `DELETE /api/books/{id}` - Delete book



Database Setup:
1. Setup SQL Server & Database
Before running the project, make sure you have SQL Server installed. If you don’t have it, you can use SQL Server Express or Azure SQL.

Open appsettings.json (or appsettings.Development.json) and add the connection string:

{
    "ConnectionStrings": {
        "DefaultConnection": "Server=YOUR_SERVER;Database=OfficeDB;Trusted_Connection=True;MultipleActiveResultSets=true"
    }
}
Replace YOUR_SERVER with your SQL Server instance name.

Run the following Entity Framework Core commands to create the database:


dotnet ef migrations add InitialCreate
dotnet ef database update
2. Install Dependencies
Run this in the terminal inside your project folder:


dotnet restore
3. Run the Project
Now start the project using:


dotnet run
Or if you're using Visual Studio, just press Ctrl + F5.

4. Test the API
Once the project is running, open a browser or use Postman to test the API endpoints:

GET all Books:
GET http://localhost:5000/api/Books
GET Books by ID:
GET http://localhost:5000/api/Books/{id}
POST new Books:
POST http://localhost:5000/api/Books
Body (JSON):

{
    "name": "Wheel Of Time",
    "Genre": "Fantasy",
    "Available Copies": 5
}
PUT update Books:
PUT http://localhost:5000/api/Books/{id}
DELETE a Book:
DELETE http://localhost:5000/api/Book/{id}



