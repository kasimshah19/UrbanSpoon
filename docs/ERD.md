# Urban Spoon — Entity-Relationship Diagram (ERD)

This diagram shows the conceptual database schema and relationships for the application, representing the MongoDB collections.

```mermaid
erDiagram
    USER {
        ObjectId _id PK
        String name
        String email
        String password
        String role "Enum: ['admin', 'customer']"
        Date createdAt
        Date updatedAt
    }

    RESERVATION {
        ObjectId _id PK
        String name
        String email
        String phone
        Date date
        String time
        Number guests
        String specialRequests
        String status "Enum: ['pending', 'confirmed', 'cancelled']"
        Date createdAt
    }

    MENU_ITEM {
        ObjectId _id PK
        String name
        String description
        Number price
        String category "Enum: ['starter', 'main', 'dessert', 'beverage']"
        String imageUrl
        Boolean isVegetarian
        Boolean isAvailable
    }

    %% Relationships
    USER ||--o{ RESERVATION : "makes"
```

## Description
- **USER**: Stores both admin and customer credentials. Roles distinguish access levels.
- **RESERVATION**: Stores table booking details. Tied conceptually to a user if logged in, but can also be made by guest users.
- **MENU_ITEM**: Stores the catalogue of dishes available in the restaurant.
