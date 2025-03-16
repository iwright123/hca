# HCA Student Web App Documentation


# Prerequisites -
.NET SDK (Download: dotnet.microsoft.com)
Visual Studio (Download: visualstudio.microsoft.com)
SQL Server Management Studio (SSMS)
Postman (For testing API requests)

git clone https://github.com/iwright123/hca.git

Modify appsettings.json to connect to your local SQL Server:

# "ConnectionStrings": {
    "Default": "data source={REPLACE With Your Server Name};Initial Catalog=StudentDB; Integrated Security=True; TrustServerCertificate=True"
  }

# Restore Dependencies
dotnet restore

# Apply Database Migrations
dotnet ef migrations add InitialCreate
dotnet ef database update

# Build and Run the Application
dotnet build

# Run the Application
dotnet run


# API -
Controller: ApiController
 Route: api/students
Base URL: https://localhost:5001/api/students

GET /api/students/{id} | GET /api/students/1

POST /api/students

{
  "name": "Charlie",
  "age": 40,
  "email": "charlie@ehca.com"
}

PUT /api/students/{id} | PUT /api/students/3

DELETE /api/students/{id} | DELETE /api/students/3

