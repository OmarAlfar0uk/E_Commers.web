# E_Commers.web

![.NET](https://img.shields.io/badge/.NET-8.0-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)
![C#](https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=c-sharp&logoColor=white)
![Entity Framework Core](https://img.shields.io/badge/EF_Core-8.0-3FA037?style=for-the-badge&logo=nuget&logoColor=white)
![SQL Server](https://img.shields.io/badge/SQL_Server-CC2927?style=for-the-badge&logo=microsoft-sql-server&logoColor=white)

A modern E-commerce Web API engineered with .NET 8, implementing Clean Architecture/Onion Architecture. The system provides a scalable product catalog featuring product brands, types, and generic base entities following Domain-Driven Design concepts.

## 🏗️ Architecture

```mermaid
graph TD
    P[Infrastructure/Presentation] --> SA[Core/ServiceAbstraction]
    SA --> D[Core/DomainLayer]
    S[Core/Service] --> SA
    S --> D
    I[Infrastructure/Persistence] --> D
    H[E-Commers.web02 Host] --> P
    H --> I
    H --> S
```

## 📂 Project Structure

| Layer | Project | Description |
|---|---|---|
| **Domain** | `Core/DomainLayer` | Entities (`BaseEntity`, `Product`, `ProductBrand`, `ProductType`). |
| **Service Interfaces** | `Core/ServiceAbstraction` | Abstractions and contracts for domain services. |
| **Service Implementation** | `Core/Service` | Business logic and use case implementations. |
| **Data Access** | `Infrastructure/Persistence` | EF Core integrations targeting SQL Server. |
| **API** | `Infrastructure/Presentaion` | Controller logic separating routing from business rules. |
| **Shared** | `Shared/Shared` | Cross-cutting concerns and shared models. |
| **Host** | `E-Commers.web02` | Startup, configuration, and API bootstrapping. |

## 🚀 Getting Started

### Prerequisites
- [.NET 8 SDK](https://dotnet.microsoft.com/download/dotnet/8.0)
- SQL Server

### Installation & Execution

```bash
# 1. Clone the repository
git clone https://github.com/OmarAlfar0uk/E_Commers.web.git

# 2. Navigate to the project root
cd E_Commers.web

# 3. Restore dependencies
dotnet restore

# 4. Run the application
dotnet run --project E-Commers.web02
```

---

## 👨‍💻 Author

**Omar Alfarouk**
- GitHub: [OmarAlfar0uk](https://github.com/OmarAlfar0uk)
- LinkedIn: [omar-alfarouk-252471251](https://www.linkedin.com/in/omar-alfarouk-252471251/)
- Email: [omaralfarouk646@gmail.com](mailto:omaralfarouk646@gmail.com)
