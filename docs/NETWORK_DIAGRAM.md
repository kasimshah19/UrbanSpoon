# Urban Spoon — Network Topology Diagram

This diagram shows how the system components communicate over the network in a typical cloud deployment.

```mermaid
graph TD
    subgraph Internet
        Users[Web Clients]
    end

    subgraph Edge
        CDN[Vercel CDN / WAF]
    end

    subgraph Backend Cloud Provider
        API_Server[Node.js / Express API Server]
    end

    subgraph Database Cloud Provider
        DB_Cluster[(MongoDB Atlas Cluster)]
    end

    Users -->|HTTPS / Port 443| CDN
    CDN -->|HTTPS| API_Server
    API_Server -->|TCP / Port 27017 (TLS)| DB_Cluster
```
