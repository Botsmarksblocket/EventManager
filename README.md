# Event Manager
[![.NET](https://img.shields.io/badge/.NET-9.0-512BD4?logo=.net)](https://dotnet.microsoft.com/download)
[![Blazor](https://img.shields.io/badge/Blazor-WASM-512BD4?logo=blazor)](https://dotnet.microsoft.com/apps/aspnet/web-apps/blazor)
[![MongoDB](https://img.shields.io/badge/MongoDB-%234ea94b.svg?logo=mongodb&logoColor=white)](#)
![bcrypt version](https://img.shields.io/badge/4.0.3-0?label=bcrypt&style=for-the-badge&labelColor=white&color=black)

## Project Overview

Event Manager is a web application designed to simplify event management and ticket purchasing. This project aims to create a user-friendly platform for both event attendees and administrators.

### Key Features

- **For Users:**

  - Browse and search for public events
  - Purchase tickets for desired events
  - Manage and track purchased tickets
  - Authenication via 

- **For Administrators:**
  - Publish, update, and remove events
  - Manage registered users
  - Monitor ticket sales and event attendance

## Technical aspects

 - Frontend: Blazor WASM
 - Backend: .NET 9 minimal API
 - Database: MongoDB
 - Authentication: User credentials are validated by the backend using BCrypt password hashing to securely store and compare passwords. Upon successful login, the server generates a signed JWT containing user identity and claims (such as roles). The token is returned to the client and included in the Authorization header for subsequent requests.

 - Authorization:  Access control is enforced using the role claim embedded in the JWT. ASP.NET Core’s [Authorize] attribute and policy-based authorization check the role claim to determine if the authenticated user has permission to access a given endpoint or Blazor component.

## Images
<details>
<summary>Click to expand</summary>
<img src="https://github.com/user-attachments/assets/d4050fc0-2927-416d-910b-c46e0e3937d8" width="800" alt="homepage" />
<img src="https://github.com/user-attachments/assets/0665bf01-8654-4b1d-8ba2-b55f872e17c9" width="800" alt="ghost" />
<img src="https://github.com/user-attachments/assets/e670ae87-bdcf-4d5c-a72c-46371ff01b62" width="800" alt="manage_users" />
<img src="https://github.com/user-attachments/assets/b6b74b39-8961-4b6d-9858-bac0c3f2bc30" width="800" alt="manage_events" />
</details>



## Getting Started

**To configure your connection string:**
In the EventManager.Api project:

1. Create a new file named 'appsettings.Development.json' if it doesn't exist.
2. Add your MongoDB connection string to this file using the following format:
   {
     "MongoDbSettings": {
       "ConnectionString": "your_mongodb_connection_string_here",
       "DatabaseName": "EventManager"
     }
   }
3. Replace 'your_mongodb_connection_string_here' with your actual MongoDB connection string.
4. Ensure this file is not tracked by Git to keep your connection string private.
