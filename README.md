# ASP.NET Core MVC AI Photo Hub

This project is an ASP.NET Core MVC web application developed as a university assignment for managing AI-generated photos. It allows users to browse, upload, and manage a gallery of AI-created images. The app uses **ASP.NET Core MVC**, an open-source, cross-platform framework for building modern web apps, and **ASP.NET Core Identity** for authentication and role-based authorization. The interface is built with **Bootstrap**, providing a responsive, mobile-friendly design. Different user roles (e.g. Admin vs. Member) determine access: Admin users can create, edit, and delete photos, while regular members can view and interact with the gallery according to their permissions.

## Key Features

- **User Authentication & Authorization:** Implements ASP.NET Core Identity for user accounts. Two example users are preconfigured (admin@asp.net / *Wdp-2024*, and member@asp.net / *Wdp-2024*). The admin user has elevated privileges to manage content; regular users have limited access as per assignment requirements.
- **Photo Gallery (CRUD):** Users can create, read, update, and delete photo entries. Admins can add new AI-generated images (by uploading or linking images), edit existing entries (titles, descriptions), or delete images. All users can view the gallery and photo details. Data operations are handled via **Entity Framework Core** as an ORM.
- **Responsive Design:** The UI uses Bootstrap’s grid system to adapt to various screen sizes. The gallery displays images in a fluid grid layout; on smaller devices the layout adjusts automatically to remain user-friendly.
- **Database Persistence:** Photo metadata and user information are stored in a **SQLite** database (app.db) for simplicity. SQLite is a lightweight, high-reliability SQL database engine suitable for local development.
- **Technology Integration:** The app leverages modern web technologies (.NET 8, C#, EF Core, Razor Views) for a clean MVC architecture, and incorporates open-source libraries (Bootstrap for styling, Identity for auth) to streamline development and ensure maintainability.

## Technologies Used

- **.NET 8.0 / ASP.NET Core MVC** – Framework for server-side logic, Controllers/Views, and routing.
- **Entity Framework Core (EF Core)** – Object-Relational Mapper for database access, enabling LINQ data operations.
- **SQLite** – Embedded SQL database for storing photos and user data; self-contained and serverless.
- **ASP.NET Core Identity** – Built-in library for managing user accounts, login, and roles.
- **Bootstrap (v5+)** – CSS/JS library for responsive, mobile-first design and components.
- **Visual Studio / VS Code** – Recommended IDEs for development.

## Installation and Setup

1. **Prerequisites:** [.NET 8.0 SDK](https://dotnet.microsoft.com/download). Optional: Visual Studio 2022+ or VS Code with C# extension.
2. **Clone the repository:**  
   ```bash
   git clone https://github.com/Yalawai/ASP.Net-Core-MCV.git
   cd ASP.Net-Core-MCV
   ```
3. **Build and run:**  
   - Visual Studio: Open `WDP2024Assignment2.generated.sln`, run project.
   - CLI:
     ```bash
     dotnet restore
     dotnet run
     ```
4. **Database:** To regenerate SQLite DB:
   ```bash
   dotnet ef database update
   ```
5. **Sample Logins:**  
   - Admin: `admin@asp.net` / `Wdp-2024`  
   - Member: `member@asp.net` / `Wdp-2024`




## Project Structure

- `/Controllers/` – MVC controllers.
- `/Models/` – Photo models and view models.
- `/Data/` – Database context and migrations.
- `/Views/` – Razor views.
- `/Areas/Identity/` – ASP.NET Identity Razor Pages.
- `Program.cs` – Startup logic.
- `appsettings.json` – Configuration.
- `app.db` – SQLite DB.


## Acknowledgments

- University of Canberra - WDP2024 Course
- [ASP.NET Core MVC Docs](https://learn.microsoft.com/aspnet/core)
- [Bootstrap](https://getbootstrap.com)
- [EF Core](https://docs.microsoft.com/ef/core)

