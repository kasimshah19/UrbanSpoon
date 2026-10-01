# Urban Spoon — Deployment Diagram

This diagram illustrates how the Urban Spoon application is typically hosted and deployed in a production environment.

```mermaid
flowchart TD
    %% End Users
    UserBrowser((User's Browser))
    AdminBrowser((Admin's Browser))
    
    %% Internet Edge
    CDN[Content Delivery Network / Edge]
    
    %% Hosting Environments
    subgraph FrontendHosting [Frontend Hosting (e.g., Vercel / Netlify)]
        StaticAssets[Static Assets HTML/CSS/JS]
        ReactApp[React SPA]
    end
    
    subgraph BackendHosting [Backend Hosting (e.g., Render / Heroku)]
        NodeServer[Node.js / Express Server]
    end
    
    subgraph DBHosting [Database Hosting (MongoDB Atlas)]
        PrimaryDB[(Primary Replica Set)]
    end
    
    %% Connections
    UserBrowser -->|HTTPS| CDN
    AdminBrowser -->|HTTPS| CDN
    
    CDN -->|Serves App| FrontendHosting
    
    UserBrowser -->|REST API Requests| BackendHosting
    AdminBrowser -->|REST API Requests| BackendHosting
    
    BackendHosting -->|Mongoose Connection| DBHosting
```

## Description
- **Frontend**: The React app is compiled into static files and served globally via a CDN (like Vercel).
- **Backend**: The Node.js server runs in a cloud environment (like Render), processing business logic and authentication.
- **Database**: Hosted on MongoDB Atlas, ensuring high availability and secure network access.
