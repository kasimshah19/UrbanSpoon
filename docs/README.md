# Urban Spoon — Diagrams & Architecture Documentation

This directory (`docs/`) contains all the software engineering and architectural diagrams for the Urban Spoon project. Each diagram serves a specific purpose in illustrating how the system operates, communicates, and is structured. 

Below is a detailed explanation of every diagram included in this repository and what it represents:

---

## 1. System Architecture (`ARCHITECTURE.md`)
**What it represents:**  
This diagram provides a high-level view of the entire MERN Stack (MongoDB, Express, React, Node.js) system. It breaks down the application into three main tiers: Frontend, Backend, and Database.
**Why it is useful:** It helps developers and stakeholders understand the foundational technologies being used and how they connect to one another on a macro level.

## 2. Data Flow Diagram (`DATA_FLOW.md`)
**What it represents:**  
This is a Level-1 Data Flow Diagram (DFD). It illustrates how data—such as user credentials and reservation forms—travels from the external entities (Customer/Admin) into the system's processes, and where it is eventually stored (Database).
**Why it is useful:** It makes it easy to track the lifecycle of data and understand what happens behind the scenes when a user performs an action on the website.

## 3. Sequence Diagram (`SEQUENCE_DIAGRAM.md`)
**What it represents:**  
This diagram shows the strict, step-by-step chronological order of events during a Table Reservation process. It maps out how a request originates from the Customer, hits the Frontend, is sent to the Backend API, is saved in the Database, and finally, how the Admin retrieves it.
**Why it is useful:** It clarifies the exact sequence of API calls and backend logic required to fulfill a specific use case.

## 4. Workflows (`WORKFLOW.md`)
**What it represents:**  
Contains State Diagrams mapping out the complete journeys for both Customers and Administrators. It tracks how a user navigates from the Homepage, to Login, to Form Submission, and back to the Dashboard.
**Why it is useful:** It visualizes the user experience (UX) flow and screen-to-screen navigation logic.

## 5. Entity-Relationship Diagram (`ERD.md`)
**What it represents:**  
This diagram models the conceptual database schema. It shows the core collections (Users, Reservations, Menu Items), their internal fields, and the logical relationships between them.
**Why it is useful:** It acts as a blueprint for the NoSQL database design, ensuring developers understand data types and associations.

## 6. Component Diagram (`COMPONENT_DIAGRAM.md`)
**What it represents:**  
A visual breakdown of the React Frontend. It maps out the hierarchy of UI components, starting from the main `App` and `Router`, down to the `Navbar`, `Pages`, and individual reusable components like `MenuCard` or `InquiryForm`.
**Why it is useful:** It helps Frontend engineers quickly navigate the React source code and understand component composition.

## 7. Deployment Diagram (`DEPLOYMENT.md`)
**What it represents:**  
This diagram illustrates the cloud infrastructure and hosting environments. It shows the Frontend hosted on a CDN (like Vercel), the Backend running in a Node.js cloud environment (like Render), and the Database hosted securely on MongoDB Atlas.
**Why it is useful:** It is essential for DevOps and deployment strategies, showing exactly where code lives in production.

## 8. Use Case Diagram (`USE_CASE.md`)
**What it represents:**  
This diagram defines the primary actors in the system (Guest, Customer, Admin) and maps out the specific actions (use cases) they are authorized to perform.
**Why it is useful:** It clearly defines system boundaries, features, and role-based access control requirements.

## 9. Class Diagram (`CLASS_DIAGRAM.md`)
**What it represents:**  
A detailed look at the Backend source code structure. It outlines the Controllers (Auth, Reservation, Menu) and Data Models, detailing their attributes and methods.
**Why it is useful:** It helps Backend developers understand Object-Oriented principles and the internal mechanics of the API endpoints.

## 10. State Diagram (`STATE_DIAGRAM.md`)
**What it represents:**  
This diagram specifically tracks the lifecycle of a single "Table Reservation". It shows how a reservation moves from a 'Pending' state to 'Confirmed' or 'Rejected', and eventually to 'Completed' or 'Cancelled'.
**Why it is useful:** It helps prevent logical bugs by providing a clear rulebook for status updates in the application.

## 11. Activity Diagram (`ACTIVITY_DIAGRAM.md`)
**What it represents:**  
A flowchart representing the decision-making process for booking a table (e.g., checking if a user is logged in before allowing them to book).
**Why it is useful:** It provides a direct map for writing `if/else` conditional logic and validation checks in the code.

## 12. Feature Mindmap (`MINDMAP.md`)
**What it represents:**  
A tree-like visual breakdown of the entire project, splitting it into Frontend, Backend, Core Features, and Deployment stacks.
**Why it is useful:** It serves as a quick, high-level summary of the project's scope, perfect for presentations or initial onboarding.

## 13. Git Branching Strategy & Timelines (`GIT_GRAPH.md`, `GANTT_CHART.md`, etc.)
**What it represents:**  
- **Git Graph**: Shows the version control history, feature branches, and merge strategies.
- **Gantt Chart**: Outlines the project development schedule (Planning, Backend, Frontend, Testing).
- **Network / C4 / Timeline**: Covers advanced networking topology, enterprise-level C4 context, and customer journey milestones.
**Why it is useful:** Essential for project management, teamwork coordination, and understanding the development lifecycle.

---
*Created for Urban Spoon - Development & Documentation*
