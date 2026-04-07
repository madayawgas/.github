# MadayawGas GitHub Organization

This organization hosts the source code for the Madayaw Gas software system.  
The project is currently structured into three independent repositories to keep responsibilities clear and development workflows clean.

---

## Repositories

### **1. madayawgas-frontend**
Web interface used by customers and internal users.  
Handles UI, client-side logic, API consumption, and session handling.

### **2. madayawgas-backend**
Service layer providing business logic, authentication, and database interaction.  
Exposes REST endpoints that follow the shared API specifications.

### **3. madayawgas-api-contracts**
Source of truth for all API definitions (OpenAPI/Swagger).  
Both frontend and backend reference this repo to maintain consistent request and response formats.

---

## Development Model

- **Polyrepo architecture**  
  Each component has its own repository, issue tracking, and CI/CD pipeline.

- **API-first workflow**  
  Any changes to endpoints or payloads start in the `api-contracts` repo before implementation.

- **Independent deployments**  
  Frontend and backend can be updated or released without affecting the other as long as both adhere to the shared contract.

---

## Contribution Workflow

1. Work inside the repo relevant to your component.  
2. Create a feature branch with a clear name (e.g., `feature/add-order-tracking`).  
3. Follow the existing code style and folder structure.  
4. Open a pull request and request a reviewer.  
5. Make sure changes align with the API contract if endpoints are involved.

---

## Documentation

System architecture decisions, diagrams, and development notes are kept inside each repo as needed.  
Use `api-contracts` for anything related to endpoint structure or integration rules.

---

## Purpose of This Organization

This org serves as a central workspace for the engineering team building the Madayaw Gas system.  
It keeps the project modular, maintainable, and consistent across its frontend, backend, and shared API definitions.
