# InsuranceProject-master

A comprehensive insurance management system built with .NET technologies, featuring a Blazor client application, MVC admin interface, and Web API with MySQL database connectivity.

## Table of Contents
- [About](#about)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Configuration](#configuration)
- [Running the Project](#running-the-project)
- [Database Setup](#database-setup)
- [Running Tests](#running-tests)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## About

InsuranceProject-master is a full-featured insurance management application that provides policy management, claims processing, customer management, and administrative functions. The system is built with a modern .NET architecture using Scaffolding for efficient database connectivity.

## Features

- **Client Portal (Blazor)**: Interactive web interface for customers
- **Admin Dashboard (MVC)**: Comprehensive administrative interface
- **RESTful Web API**: Backend services with MySQL database
- **Policy Management**: Create, update, and manage insurance policies
- **Claims Processing**: Intake, tracking, and processing of insurance claims
- **Customer Management**: Customer profiles and policy management
- **Authentication & Authorization**: Secure access control
- **Database Scaffolding**: Automated data layer generation

## Tech Stack

- **Backend**: .NET Web API, ASP.NET Core MVC
- **Frontend**: Blazor (Client), Razor Pages (Admin)
- **Database**: MySQL with Entity Framework Core
- **ORM**: Entity Framework Core with Scaffolding
- **IDE**: Visual Studio
- **Authentication**: ASP.NET Core Identity (if implemented)
- **Build Tools**: .NET CLI, MSBuild

## Prerequisites

- **.NET SDK 6.0+** or **7.0+** (check project files for exact version)
- **Visual Studio 2022** (recommended) or VS Code
- **MySQL Server** 8.0+ (local installation or Docker)
- **MySQL Workbench** (optional, for database management)
- **Git** for version control

## Installation

1. **Clone the repository**:
```bash
git clone https://github.com/MGChaitra/InsuranceProject-master.git
cd InsuranceProject-master
```

2. **Restore NuGet packages**:
```bash
dotnet restore
```

3. **Build the solution**:
```bash
dotnet build
```

## Configuration

1. **Database Connection**:
   - Update the connection string in `appsettings.json`:
   ```json
   {
     "ConnectionStrings": {
       "DefaultConnection": "Server=localhost;Database=InsuranceDB;Uid=your_username;Pwd=your_password;"
     }
   }
   ```

2. **Environment Configuration**:
   - For development, use `appsettings.Development.json`
   - For production, use environment variables or `appsettings.Production.json`

## Database Setup

1. **Create MySQL Database**:
```sql
CREATE DATABASE InsuranceDB;
```

2. **Run Entity Framework Migrations** (if using Code First):
```bash
dotnet ef database update
```

3. **Scaffolding** (if using Database First approach):
```bash
dotnet ef dbcontext scaffold "YourConnectionString" Pomelo.EntityFrameworkCore.MySql -OutputDir Models -ContextDir Data -Context InsuranceDbContext -Force
```

## Running the Project

### Using Visual Studio:
1. Open `InsuranceProject.sln` in Visual Studio
2. Set multiple startup projects:
   - Blazor Client App
   - MVC Admin App  
   - Web API Project
3. Press F5 or click "Run"

### Using .NET CLI:

1. **Run Web API**:
```bash
cd YourApiProject
dotnet run
```

2. **Run Blazor Client** (in new terminal):
```bash
cd YourBlazorProject
dotnet run
```

3. **Run MVC Admin** (in new terminal):
```bash
cd YourMvcProject
dotnet run
```

### Access Points:
- **Blazor Client**: http://localhost:5001 (or configured port)
- **MVC Admin**: http://localhost:5002 (or configured port) 
- **Web API**: http://localhost:5000 (or configured port)

## Running Tests

### Unit Tests:
```bash
dotnet test
```

### Specific Test Project:
```bash
cd YourTestProject
dotnet test
```

## Project Structure

```
InsuranceProject-master/
├── Insurance.API/                 # Web API Project
│   ├── Controllers/
│   ├── Models/
│   ├── Services/
│   └── Program.cs
├── Insurance.Blazor/              # Blazor Client App
│   ├── Pages/
│   ├── Shared/
│   ├── Services/
│   └── Program.cs
├── Insurance.Mvc/                 # MVC Admin App
│   ├── Controllers/
│   ├── Views/
│   ├── Models/
│   └── Program.cs
├── Insurance.Data/                # Data Access Layer
│   ├── Models/ (Scaffolded)
│   ├── Context/
│   └── Migrations/
├── Insurance.Core/                # Business Logic
│   ├── Services/
│   ├── Interfaces/
│   └── Models/
├── Tests/                         # Test Projects
│   ├── UnitTests/
│   └── IntegrationTests/
├── appsettings.json              # Configuration
└── InsuranceProject.sln          # Solution File
```

## Contributing

We welcome contributions! Please follow these guidelines:

1. **Fork the repository**
2. **Create a feature branch**:
```bash
git checkout -b feature/your-feature-name
```

3. **Make your changes and commit**:
```bash
git commit -m "Add: description of your changes"
```

4. **Push and open a Pull Request**

### Development Guidelines:
- Follow .NET coding conventions
- Use meaningful commit messages
- Add tests for new functionality
- Update documentation as needed
- Ensure all tests pass before submitting PR

## Issues & Support

- For bug reports, use GitHub Issues with detailed descriptions
- Include steps to reproduce, expected vs actual behavior
- Provide environment details (.NET version, MySQL version, etc.)

## License

This project is licensed under the [Specify License - MIT/Proprietary]. Please add a LICENSE file to the repository root.

## Contact

**Maintainer**: MGChaitra  
**Repository**: https://github.com/MGChaitra/InsuranceProject-master

For questions or support, please open an issue in this repository.

---

*Note: This README provides a comprehensive starting point. Update specific project names, ports, and configuration details to match your actual project structure.*
