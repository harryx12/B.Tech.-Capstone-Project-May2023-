# E-Waste Management Web Platform

A research and development project focused on the status, management strategies, and recycling of waste Printed Circuit Boards (PCBs) in India, accompanied by a web-based platform to streamline e-waste collection and disposal.

---

## Overview

India generated over 16 lakh tonnes of e-waste in 2021–22, with a significant gap between what is generated and what is formally collected and recycled. Most e-waste recycling in India is carried out by the informal sector using crude, hazardous methods, resulting in loss of precious metals and serious health and environmental risks.

This project addresses those challenges through:

- A comprehensive literature survey and field study of e-waste management in India
- Review of metal recovery and recycling processes for waste PCBs
- A proposed design flowchart integrating formal and informal recycling sectors
- A full-stack web platform to connect consumers, dealers, dismantlers, and recyclers

---

## Problem Statement

- E-waste contains valuable metals (gold, silver, copper, platinum, palladium) as well as toxic substances (lead, mercury, brominated flame retardants).
- The informal sector recovers only a fraction of available materials and causes significant health and environmental damage.
- There is no efficient mechanism to channel e-waste from consumers to certified formal recyclers.

---

## Key Findings

- An integrated approach combining the informal sector (collection, dismantling, segregation) with the formal sector (metal extraction, recycling) is the most effective model.
- Extended Producer Responsibility (EPR) regulations place accountability on manufacturers, producers, and consumers, but enforcement remains a challenge.
- Hydrometallurgical, Pyrometallurgical, and Electrometallurgical processes are used to recover base and precious metals from PCBs.
- Field research conducted in Mumbai (Dharavi area) revealed ground-level challenges in e-waste handling.

---

## Web Platform

### Purpose

The E-Waste Management Web Platform connects all stakeholders in the e-waste value chain — from consumers who want to dispose of old devices to certified recyclers — enabling transparent, trackable, and environmentally sound e-waste handling.

### User Roles

| Role | Description |
|------|-------------|
| **Admin** | Controls all platform activity; manages user registrations and assignments |
| **Consumer** | Domestic users, government offices, industries, and manufacturers who list e-waste items for sale |
| **Kabadiwala** | Registered collectors who purchase e-waste from consumers |
| **Dealer** | Purchases e-waste from Kabadiwalas; routes items to dismantlers or recyclers |
| **Dismantler** | Receives and dismantles items from dealers |
| **Recycler** | Receives items from dealers/dismantlers for formal metal extraction and recycling |

### System Architecture

The platform follows a three-layer architecture:

- **Presentation Layer** — User interface built with HTML, CSS, and JavaScript/jQuery
- **Application Layer** — Business logic handled using C# .NET (MVC 2016)
- **Data Layer** — Data management using MSSQL

---

## Tech Stack

| Component | Technology |
|-----------|-----------|
| Frontend | HTML, CSS, JavaScript, jQuery, Bootstrap |
| Backend | C# .NET, ASP.NET MVC 2016 |
| Database | MSSQL (SQL Server) |
| Architecture | MVC (Model-View-Controller) |

---

## Project Structure

```
E_WasteManagement/
├── Controllers/
│   ├── AdminController.cs
│   ├── ConsumerController.cs
│   ├── UserController.cs
│   ├── MasterController.cs
│   ├── BillController.cs
│   ├── ReportController.cs
│   └── ... (other controllers)
├── Models/
│   ├── IdentityModels.cs
│   ├── AccountViewModels.cs
│   └── Helper.cs
├── Scripts/
│   ├── Consumer.js
│   ├── User.js
│   └── ... (other JS files)
├── ClassLibrary/
│   ├── Core.Business/
│   ├── Core.CommonConstants/
│   └── Core.CommonUtilities/
└── E_WasteManagement.csproj
```

---

## Setup & Requirements

### Hardware Requirements

- **Web Server** — Sufficient processing power and memory to handle concurrent requests
- **Database Server** — Reliable storage for user data, e-waste collection records, and recycling information
- **Storage Devices** — Adequate space for platform data

### Software Requirements

- Visual Studio 2016 or later
- .NET Framework (MVC 2016)
- SQL Server (MSSQL)
- IIS or compatible web server for deployment

### Getting Started

1. Clone or extract the repository.
2. Open `E_WasteManagement.sln` in Visual Studio.
3. Restore NuGet packages.
4. Update the connection string in `Web.config` to point to your SQL Server instance:
   ```xml
   <connectionStrings>
     <add name="SqlConnectionString" connectionString="your_connection_string_here" />
   </connectionStrings>
   ```
5. Run the database migrations or execute the provided SQL scripts to set up the schema.
6. Build and run the project.

---

## References

1. Global E-Waste Statistics — [theroundup.org](https://theroundup.org/global-e-waste-statistics/)
2. Chatterjee, A.; Abraham, J. — *Efficient management of e-wastes*, International Journal of Environmental Science and Technology, 2017.
3. Tansel B — *From electronic consumer products to e-wastes: global outlook*, Environment International, 2017.
4. Patil, R.A; Ramakrishna S — *A comprehensive analysis of e-waste legislation worldwide*, Environmental Science and Pollution Research, 2020.
5. Siddharth Ghanshyam Singh — *E-Waste Management in India: Challenges and Agenda*, Centre for Science and Environment, 2020.
6. E-waste Roadmap 2023 of India — [greene.gov.in](https://greene.gov.in)

---

## License

This project is intended for academic and research purposes.
