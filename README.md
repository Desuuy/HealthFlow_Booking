# HealthFlow Booking

[![.NET](https://img.shields.io/badge/.NET-8.0-blue.svg)](https://dotnet.microsoft.com/download/dotnet/8.0)
[![ASP.NET Core](https://img.shields.io/badge/ASP.NET%20Core-8.0-green.svg)](https://dotnet.microsoft.com/apps/aspnet)
[![SQL Server](https://img.shields.io/badge/SQL%20Server-2019+-orange.svg)](https://www.microsoft.com/en-us/sql-server)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

## Description

**HealthFlow Booking** is a comprehensive web-based medical appointment platform built with **ASP.NET Core 8.0**. The system enables patients to schedule appointments with specialists, manage personal health records, and provides dedicated management portals for doctors and administrators.

---

## Key Features

### For Patients
- **Secure Authentication**: Robust Sign-up and Login system.
- **Easy Booking**: Schedule appointments by selecting doctors, specialties, and preferred time slots.
- **Profile Management**: View medical history and personal health records.
- **Smart Search**: Filter doctors by specialty or hospital location.
- **Feedback System**: Rate and review services after consultations.
- **AI Disease Prediction**: Integrated AI feature to predict potential conditions based on symptoms.
- **Password Recovery**: Secure account recovery via email.

### For Doctors
- **Appointment Management**: View, confirm, or cancel patient schedules.
- **Patient Insights**: Access detailed medical records of patients.
- **Revenue Analytics**: Track and monitor monthly income and statistics.
- **Real-time Notifications**: Instant alerts for new appointment requests.
- **Profile Customization**: Manage professional information and biography.

### For Administrators
- **User Management**: Oversee Patients, Doctors, and Admin accounts.
- **Facility Management**: Create and update hospital/clinic details.
- **Department Management**: Manage medical specialties and categories.
- **Content Management**: Publish medical articles and health tips.
- **Executive Dashboard**: Overview reports on revenue and consultation volume.
- **Transaction Logs**: Monitor and manage all system payments.

---

## Technology Stack

### Backend
- **ASP.NET Core 8.0**: Main web framework.
- **C#**: Primary programming language.
- **Entity Framework Core**: ORM for database operations.
- **SignalR**: Real-time communication for notifications.
- **Session Management**: Secure user session handling.

### Frontend
- **HTML5 / CSS3**: Core structure and styling.
- **JavaScript / jQuery**: Client-side interactivity.
- **Bootstrap**: Responsive UI design framework.
- **Razor Views**: Dynamic server-side rendering.

### Database
- **SQL Server**: Primary relational database management system.
- **Stored Procedures**: Optimized query execution for high performance.

---

## Getting Started

### Prerequisites
- .NET 8.0 SDK
- SQL Server 2019 or higher
- Visual Studio 2022 or VS Code

### Clone the Repository
```bash
git clone https://github.com/Desuuy/HealthFlow_Booking
```

### Database Configuration
- Create a new database in your SQL Server instance.
- Run the All_StoredProcedures.sql script (found in the SQL Scripts folder) to initialize procedures and tables.
- Update the DefaultConnection string in appsettings.json:
```
{
  "ConnectionStrings": {
    "DefaultConnection": "Server=YOUR_SERVER;Database=VinMecDB;Trusted_Connection=true;TrustServerCertificate=true;"
  }
}
```
### Install Dependencies
```
dotnet restore
```
### Run the Application
```
dotnet run
```

### Project Structure
```
VinMec/
├── Controllers/          # Logic handlers (Home, Admin, Doctor, API)
├── Models/               # Data entities and AI prediction models
├── Views/                # Razor templates (Patient, Admin, and Doctor portals)
├── wwwroot/              # Static files (CSS, JS, Images, Uploads)
├── SQL Scripts/          # Database initialization and Stored Procedures
├── Program.cs            # Entry point and service configuration
└── appsettings.json      # Configuration settings (Connection Strings)
```

### Security & Configuration
- Encrypted Sessions: Secure login state management with a 30-minute timeout.
- Password Hashing: Protects user credentials within the database.
- Input Validation: Prevents common web vulnerabilities (XSS, SQL Injection).
- HTTPS Redirection: Ensures all communication is encrypted in transit.
