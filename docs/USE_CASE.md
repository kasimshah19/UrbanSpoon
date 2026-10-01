# Urban Spoon — Use Case Diagram

This diagram shows the primary actors in the system and the specific actions (use cases) they can perform.

```mermaid
usecaseDiagram
    actor Customer
    actor Admin
    actor Guest

    %% Guest Actions
    Guest --> (View Menu)
    Guest --> (View Restaurant Info)
    Guest --> (Register Account)
    Guest --> (Submit Reservation Inquiry)

    %% Customer Actions (Inherits from Guest conceptually)
    Customer --> (View Menu)
    Customer --> (Login)
    Customer --> (Submit Reservation Inquiry)
    Customer --> (View Own Profile)

    %% Admin Actions
    Admin --> (Login as Admin)
    Admin --> (View All Reservations)
    Admin --> (Update Reservation Status)
    Admin --> (Manage Menu Items)
    Admin --> (View Dashboard Statistics)
```

## Description
- **Guest**: Unauthenticated users who can browse the site and submit inquiries.
- **Customer**: Authenticated regular users.
- **Admin**: Staff/Owners who have elevated privileges to manage the business operations through the backend dashboard.
