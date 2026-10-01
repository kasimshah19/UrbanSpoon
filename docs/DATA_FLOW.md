# Urban Spoon — Data Flow Diagram (DFD)

This diagram illustrates how data flows through the Urban Spoon system, particularly focusing on the reservation and authentication processes.

## Level 1 Data Flow

```mermaid
flowchart LR
    %% Entities
    Customer((Customer))
    Admin((Admin))
    
    %% Processes
    AuthProcess(Authentication Process)
    ResProcess(Reservation Process)
    MenuProcess(Menu Management)
    
    %% Data Stores
    DB[(MongoDB Database)]
    
    %% Data Flows - Customer
    Customer -->|Login Credentials| AuthProcess
    AuthProcess -->|Token| Customer
    
    Customer -->|Reservation Details| ResProcess
    ResProcess -->|Store Request| DB
    ResProcess -->|Confirmation| Customer
    
    Customer -->|Request Menu| MenuProcess
    DB -->|Menu Items| MenuProcess
    MenuProcess -->|Display Menu| Customer
    
    %% Data Flows - Admin
    Admin -->|Admin Credentials| AuthProcess
    AuthProcess -->|Admin Token| Admin
    
    Admin -->|Request Reservations| ResProcess
    DB -->|Reservation Data| ResProcess
    ResProcess -->|Dashboard View| Admin
    
    Admin -->|Update Status| ResProcess
    ResProcess -->|Modify Record| DB
```

## Description
- **Authentication**: Users and Admins send credentials to get a JWT token.
- **Reservations**: Customers submit reservation details, which are processed and stored in the database. Admins retrieve and manage these records.
- **Menu**: Customers request the menu, which is fetched from the database and displayed.
