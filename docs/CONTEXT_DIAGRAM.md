# Urban Spoon — System Context Diagram (Level 0 DFD)

This is a high-level view showing the system in the center and its interactions with external entities.

```mermaid
flowchart TD
    Customer((Customer))
    Admin((Restaurant Admin))
    
    System[Urban Spoon System]
    
    EmailService[[Email Service / SMTP]]
    PaymentGateway[[Payment Gateway (Optional)]]

    Customer -->|Browses Menu & Books Table| System
    System -->|Sends Booking Confirmation| Customer
    
    Admin -->|Manages Reservations & Menu| System
    System -->|Displays Dashboard Analytics| Admin
    
    System -->|Sends Notifications| EmailService
    System -.->|Processes Deposits| PaymentGateway
```
