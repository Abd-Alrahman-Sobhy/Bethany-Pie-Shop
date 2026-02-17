# 🥧 Bethany's Pie Shop

<div align="center">

![ASP.NET Core](https://img.shields.io/badge/ASP.NET%20Core-MVC-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)
![C#](https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=csharp&logoColor=white)
![Blazor](https://img.shields.io/badge/Blazor-512BD4?style=for-the-badge&logo=blazor&logoColor=white)
![Entity Framework](https://img.shields.io/badge/Entity%20Framework%20Core-6B2C91?style=for-the-badge&logo=nuget&logoColor=white)
![SQL Server](https://img.shields.io/badge/SQL%20Server-CC2927?style=for-the-badge&logo=microsoftsqlserver&logoColor=white)
![SCSS](https://img.shields.io/badge/SCSS-CC6699?style=for-the-badge&logo=sass&logoColor=white)

A full-featured **online pie shop** built with **ASP.NET Core MVC**, featuring a dynamic shopping cart, user authentication, Blazor-powered search, a REST API, and a dedicated unit test project.

</div>

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
- [Configuration](#-configuration)

---

## 🌟 Overview

Bethany's Pie Shop is a full-stack **ASP.NET Core MVC** web application for an online bakery. It showcases a wide range of ASP.NET Core concepts including MVC, Razor Pages, Blazor components, Web API, Entity Framework Core, ASP.NET Core Identity, session management, and unit testing — all in a single cohesive project.

> 📚 This project is based on the **"Building an Enterprise ASP.NET Core MVC App"** course by **Gill Cleeren** on Pluralsight, extended with additional features and a test suite.

---

## 🚀 Features

### 🛒 Shopping & Orders
- Browse all available pies with images, descriptions, and prices
- Filter pies by **category**
- View detailed pie information on a dedicated product page
- Add pies to a **dynamic shopping cart** (session-based)
- Cart summary widget visible across all pages via **View Component**
- Checkout flow with **order form** and **client + server-side validation**
- Order confirmation and history

### 🔐 Authentication & Authorization
- User **registration and login** via ASP.NET Core Identity
- Authorization required to place an order (checkout protected)
- Secure password hashing and cookie-based sessions

### 🔍 Search
- **jQuery + AJAX** powered pie search
- **Blazor** component alternative for interactive search

### 📄 Pages
- Home page with featured / latest pies
- Pie list and pie detail pages
- About & Contact pages with feedback form
- Admin area for managing pies and orders

### 🧪 Testing
- Dedicated **unit test project** (`BethanysPieShopTests`)
- Tests for controllers, repositories, and core business logic
- Mock repositories for isolated testing

### 🗄️ Infrastructure
- **Entity Framework Core** with SQL Server
- **Database seeding** on application startup
- **TSQL** scripts for database setup
- **SCSS** for maintainable, structured styling
- **Web API** endpoints for pie data

---

## 🧰 Tech Stack

| Technology | Purpose |
|---|---|
| **C#** | Backend language |
| **ASP.NET Core MVC** | Web framework & routing |
| **Razor Views** | Server-side HTML rendering |
| **Blazor** | Interactive search component |
| **ASP.NET Core Web API** | REST endpoints for pie data |
| **ASP.NET Core Identity** | Authentication & authorization |
| **Entity Framework Core** | ORM & database management |
| **SQL Server** | Relational database |
| **SCSS / CSS** | Styling & theming |
| **JavaScript / jQuery** | Frontend interactivity & AJAX search |
| **xUnit / MSTest** | Unit testing |

---

## 📁 Project Structure

```
Bethany-Pie-Shop/
├── BethanysPieShop/                  # Main web application
│   ├── Controllers/                  # MVC & API controllers
│   ├── Models/                       # Domain entities & view models
│   ├── Views/                        # Razor views (.cshtml)
│   │   ├── Pie/                      # Pie list, detail, search views
│   │   ├── ShoppingCart/             # Cart & checkout views
│   │   ├── Order/                    # Order form & confirmation views
│   │   ├── Home/                     # Home & about views
│   │   └── Shared/                   # Layout, partials & view components
│   ├── Components/                   # View components (e.g. cart summary)
│   ├── Blazor/                       # Blazor search component
│   ├── Repositories/                 # Data access & mock repositories
│   ├── Data/                         # DbContext, seeding & EF configuration
│   ├── Migrations/                   # EF Core database migrations
│   ├── wwwroot/                      # Static assets
│   │   ├── css/ & scss/              # Stylesheets
│   │   ├── js/                       # JavaScript & jQuery
│   │   └── images/                   # Pie images
│   ├── appsettings.json              # App configuration
│   └── Program.cs                    # Entry point, DI & middleware pipeline
│
├── BethanysPieShopTests/             # Unit test project
│   ├── ControllerTests/              # Controller unit tests
│   ├── RepositoryTests/              # Repository unit tests
│   └── MockData/                     # Mock repositories & test data
│
└── BethanysPieShop.sln               # Solution file
```

---

## ⚡ Getting Started

### Prerequisites

- [.NET SDK](https://dotnet.microsoft.com/download)
- [SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-downloads) or SQL Server Express
- [Visual Studio 2022+](https://visualstudio.microsoft.com/) or [VS Code](https://code.visualstudio.com/)

### Installation

**1. Clone the repository**
```bash
git clone https://github.com/Abd-Alrahman-Sobhy/Bethany-Pie-Shop.git
cd Bethany-Pie-Shop
```

**2. Restore dependencies**
```bash
dotnet restore
```

**3. Update the connection string** (see [Configuration](#-configuration))

**4. Apply database migrations**
```bash
dotnet ef database update --project BethanysPieShop
```

**5. Run the application**
```bash
dotnet run --project BethanysPieShop
```

The app will be available at `https://localhost:5001`. The database will be seeded with sample pies and categories automatically on first launch.

### Running Tests

```bash
dotnet test BethanysPieShopTests
```

---

## ⚙️ Configuration

Update `appsettings.json` in the `BethanysPieShop` project:

```json
{
  "ConnectionStrings": {
    "BethanysPieShopDbContextConnection": "Server=.;Database=BethanysPieShopDB;Trusted_Connection=True;TrustServerCertificate=True;"
  }
}
```

| Key | Description |
|---|---|
| `ConnectionStrings:BethanysPieShopDbContextConnection` | Your SQL Server connection string |

---

<div align="center">

Made with ❤️ by [Abd-Alrahman Sobhy](https://github.com/Abd-Alrahman-Sobhy)

⭐ If you find this project helpful, please consider giving it a star!

</div>
