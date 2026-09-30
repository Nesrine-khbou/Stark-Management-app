# Stark ERP Administration Platform

> Final-year project (PFE): a web platform that centralizes and automates the administration of the **Stark ERP** (companies, licenses, users, roles, plans, and environments).

![Angular](https://img.shields.io/badge/Angular-21-DD0031?logo=angular&logoColor=white) ![Spring Boot](https://img.shields.io/badge/Spring_Boot-Microservices-6DB33F?logo=springboot&logoColor=white) ![Keycloak](https://img.shields.io/badge/Keycloak-OIDC-4D4D4D?logo=keycloak&logoColor=white) ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?logo=postgresql&logoColor=white) ![SQL Server](https://img.shields.io/badge/SQL_Server-CC2927?logo=microsoftsqlserver&logoColor=white) ![Tailwind](https://img.shields.io/badge/Tailwind_CSS-06B6D4?logo=tailwindcss&logoColor=white)


---

## Quick Links

| | |
|---|---|
| 📄 **PFE Report** | [View the full report](https://drive.google.com/file/d/1NTKwxCAnV4GF_kLWD95hCG--FdmVYpgY/view?usp=sharing) |
| 🎬 **Demo Video** | [Watch the demo](https://drive.google.com/file/d/1jaCAMgRCn3VzJomY-W3lZdpFtvK5QhTi/view?usp=sharing) |

---

## Academic Context

| | |
|---|---|
| **Author** | Nesrine Khbou |
| **Degree** | Engineering Degree in Computer Science (Software Engineering) |
| **Institution** | Higher Institute of Computer Science and Multimedia of Sfax (ISIMS), University of Sfax |
| **Host Organization** | Spark-it, developer of the Stark ERP (Java team) |
| **Academic Year** | 2025 / 2026 |

---

## Problem Statement

The **Stark ERP** covers several business modules, including accounting, finance, inventory, sales, purchasing, e-commerce, and human resources. However, platform administration remained largely **manual and directly performed at the database level**.

- Creating a company required technical knowledge of the architecture and relationships between database tables.

- The existing APIs also required advanced technical skills.

- There was no formal management system for **plans and licenses**.

- There was no **global overview** of the companies using Stark.

**Problem Statement:**

> How can Stark administration be simplified and automated to make it accessible to users without advanced technical skills?

---

## Proposed Solution

A **web-based administration platform** consisting of two main areas.

### Administrator Area

- Platform user management
- Company, role, and permission management
- Stark user management
- Plan and license management
- Management of DEV, TEST, QA, and PROD environments
- Data synchronization
- Free Trial configuration

### Client Area

- Overview of their companies
- Management of their Stark users, plans, and licenses
- Creation of a company through a **Free Trial**

---

## Technical Highlights

- **Centralized authentication with Keycloak**: OpenID Connect, JWT, admin/client roles, Angular guards, and API security with Spring Security.

- **Microservices architecture**: three Spring Boot services communicating through REST, with one database per service.

- **Plan and license management**: plans group sub-modules, while licenses control access to specific features.

- **Automated provisioning**: creation and monitoring of resources associated with companies, with automatic retry in case of failure.

- **Automated license lifecycle**: expiration notifications and automatic status updates.

- **Multi-environment support**: management of different Stark Auth instances using local and external identifiers.

- **Data synchronization**: synchronization of data already existing across environments.

- **Multi-company management**: a user can belong to multiple companies with different roles.

- **Free Trial**: automated creation of a trial company in an isolated environment with a dedicated license.

---