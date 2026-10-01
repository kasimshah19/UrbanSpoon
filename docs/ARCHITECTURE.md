# Urban Spoon — System Architecture

This document illustrates the high-level architecture of the Urban Spoon application. It follows a standard MERN stack structure (MongoDB, Express.js, React, Node.js).

## Architecture Diagram

```mermaid
graph TD
    %% Client Tier
    subgraph Frontend [Client-Side / Frontend]
        UI[React.js UI]
        Router[React Router DOM]
        State[React Context / State]
        Axios[Axios HTTP Client]
        
        UI --> Router
        Router --> State
        State --> Axios
    end

    %% Server Tier
    subgraph Backend [Server-Side / Backend]
        API[Express.js API]
        Auth[JWT Authentication]
        Controllers[Route Controllers]
        Mongoose[Mongoose ODM]
        
        API --> Auth
        Auth --> Controllers
        Controllers --> Mongoose
    end

    %% Database Tier
    subgraph Database [Database Tier]
        MongoDB[(MongoDB Atlas)]
    end

    %% External Connections
    User((User/Browser)) -->|HTTP/HTTPS| Frontend
    Axios -->|REST API Calls| API
    Mongoose -->|TCP/IP| MongoDB
```

## Description
- **Frontend**: Built with React and Vite. It handles routing, user interface state, and HTTP requests via Axios.
- **Backend**: Built with Node.js and Express. Handles API endpoints, user authentication (JWT), business logic, and interacts with the database.
- **Database**: MongoDB Atlas is used for scalable, cloud-based data storage, connected via Mongoose for schema definitions.
