# 📊 ExpenseFlow

**Simple. Secure. Scalable.**
A family-oriented expense tracking system built using Clean Architecture and modern full-stack technologies.

> This project is designed with a clear separation of concerns:
>
> * A **Presentation Tier** using Angular 17 + PrimeNG
> * A **Middle Tier** using Java 21 + Spring Boot 3.x
> * Both developed with a security-first, enterprise-grade mindset

---

## 🔰 Purpose

**ExpenseFlow** exists to help individuals and families:

* Track expenses across categories
* Maintain spending discipline
* Access financial insights easily, from any device
* Avoid the “spreadsheet with lipstick” problem

Unlike typical hobby budget apps, ExpenseFlow prioritizes:

* **Security**
* **Scalability**
* **Architectural clarity**

---

## 🧱 Architecture Overview

### 🧭 High-Level Structure

```plaintext
ExpenseFlow/
├── PresentationTier/   → Angular 17 + PrimeNG (frontend)
├── MiddleTier/         → Spring Boot 3.x (backend API)
└── docs/               → Design, API, security, and roadmap documentation
```

### 🧠 Clean Architecture (MiddleTier)

Layered by responsibility, inspired by Uncle Bob & Phobos design principles:

```plaintext
domain/         → Pure business logic (no Spring dependencies)  
application/    → Use case orchestration, services, DTOs  
infrastructure/ → JPA, security config, mappers  
interfaces/     → REST controllers, request handling
```

---

## ⚙️ Technologies Used

| Layer                       | Stack                                                                      |
| --------------------------- | -------------------------------------------------------------------------- |
| Frontend (PresentationTier) | Angular 17, PrimeNG 17, SCSS, Standalone Components                        |
| Backend (MiddleTier)        | Java 21, Spring Boot 3.x, Spring Security, JPA, PostgreSQL, Flyway, Lombok |
| Build Tools                 | Maven, npm                                                                 |
| Security                    | BCrypt, CSRF, CORS                                                         |
| Docs                        | Markdown, Swagger (planned), Mermaid (optional)                            |

---

## 💡 Key Features (MVP)

* [x] Add/view/delete expenses
* [x] Category and date filtering
* [x] Auth (register/login)
* [x] Security baked in from the start
* [ ] Reminders and recurring expenses (planned)
* [ ] Family-level sharing or visibility (phase II)

---

## 📁 Folder Structure

```plaintext
ExpenseFlow/
├── PresentationTier/      # Angular app (UI)
├── MiddleTier/            # Spring Boot backend (API, clean architecture)
├── docs/                  # Architecture, security, and API docs
└── README.md
```

---

## 🛠️ Getting Started

### 🔹 Prerequisites

* Node.js (v18+)
* Java 21
* PostgreSQL running locally (or Docker container)

---

### 🔹 Run Frontend

```bash
cd PresentationTier
npm install
ng serve
```

---

### 🔹 Run Backend

```bash
cd MiddleTier
./mvnw spring-boot:run
```

App will be live at:
📍 `http://localhost:4200` (frontend)
📍 `http://localhost:8080` (backend API)

---

## 🔐 Security Approach

Security is built into the architecture, not bolted on:

* CSRF protection (Angular + Spring)
* CORS policy (dev-friendly, strict in prod)
* BCrypt for password hashing
* Role-based route protection (future)
* No sensitive data ever stored client-side

See [`docs/security.md`](./docs/security.md) for full breakdown.

---

## 🔌 API Overview

| Endpoint             | Method | Description             |
| -------------------- | ------ | ----------------------- |
| `/api/auth/register` | POST   | Register a new user     |
| `/api/auth/login`    | POST   | Authenticate user       |
| `/api/expenses`      | GET    | Fetch all expenses      |
| `/api/expenses`      | POST   | Create a new expense    |
| `/api/expenses/{id}` | DELETE | Delete an expense by ID |

Full request/response examples in [`docs/api-contracts.md`](./docs/api-contracts.md)

---

## 🧭 Roadmap (High-Level)

| Phase     | Focus                                       |
| --------- | ------------------------------------------- |
| Phase I   | Auth, basic expense tracking, MVP stability |
| Phase II  | Family roles, shared visibility, reminders  |
| Phase III | Reports, charts, budgeting, multi-user SaaS |
| Phase IV  | Mobile PWA, 3rd-party bank integrations     |

Detailed roadmap in [`docs/future-roadmap.md`](./docs/future-roadmap.md)

---

## 🙋‍♂️ Dev Guide (Coming Soon)

Planned content for onboarding contributors, explaining:

* How to add new use cases (clean architecture style)
* How to add new Angular components (standalone pattern)
* How to test each layer (unit + integration)

---

## ✅ Current Status

> This project is actively under development and MVP-focused.
> Next planned milestone: **DTO → Service → Controller pipeline for Expenses**
> All commits follow `[ARCH]`, `[SECURITY]`, `[API]`, and `[DOCS]` prefixes for clarity.

---

## 🛡️ License

[MIT License](LICENSE)

---

## 🔥 Built by Devpool

Built with discipline by **Devpool Engineering**
Architected in the spirit of **Phobos, god of clean code and brutalist design.**
Security is not optional. Modules are not toys. We build with intent.
