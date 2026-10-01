# Urban Spoon — Component Diagram

This diagram visualizes the React frontend component hierarchy and how different UI pieces are composed together.

```mermaid
graph TD
    App[App Component]
    
    %% Context & Providers
    AuthContext[Auth Context Provider]
    Router[Browser Router]
    
    App --> AuthContext
    AuthContext --> Router
    
    %% Layout
    Router --> Navbar[Navbar Component]
    Router --> Main[Main Content Area]
    Router --> Footer[Footer Component]
    
    %% Pages
    Main --> Home[Home Page]
    Main --> Menu[Menu Page]
    Main --> Contact[Contact Page]
    Main --> Login[Login / Register Page]
    Main --> Admin[Admin Dashboard Page]
    
    %% Shared/Nested Components
    Home --> HeroSection[Hero Section]
    Home --> AboutSection[About Section]
    Home --> FeaturedItems[Featured Items]
    
    Menu --> MenuFilter[Menu Filter Buttons]
    Menu --> MenuCard[Menu Item Card]
    
    Contact --> InquiryForm[Reservation Form]
    Contact --> ContactInfo[Contact Details]
    
    Admin --> AdminSidebar[Admin Sidebar]
    Admin --> ReservationTable[Reservations Data Table]
    Admin --> StatsCards[Dashboard Stats]
```

## Description
- The application is wrapped in an **Auth Context** for global state management regarding user logins.
- The **Navbar** and **Footer** are persistent across pages.
- The **Admin Dashboard** is protected and only renders if the user is authenticated as an admin.
