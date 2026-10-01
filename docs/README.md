# Urban Spoon — Diagrams & Architecture Documentation

Yeh folder (`docs/`) project ke saare software engineering aur architecture diagrams ko store karta hai. Har ek diagram system ke ek alag pehlu (aspect) ko detail mein samjhata hai. 

Neeche har diagram ka detailed explanation diya gaya hai ki **kis diagram mein kya kaam ho raha hai aur wo kyun zaruri hai:**

---

## 1. System Architecture (`ARCHITECTURE.md`)
**Kya kaam ho raha hai?**  
Yeh diagram dikhata hai ki aapka poora system kaise bana hai (MERN Stack). Ismein Frontend (React/Vite), Backend (Express/Node.js API), aur Database (MongoDB) ko alag-alag blocks mein dikhaya gaya hai aur yeh samjhaya gaya hai ki wo aapas mein kaise connect hote hain.
**Fayda:** Ek developer ko system ka high-level "big picture" samajh aa jata hai.

## 2. Data Flow Diagram (`DATA_FLOW.md`)
**Kya kaam ho raha hai?**  
Yeh DFD (Level 1) batata hai ki data (jaise ki customer ka login credentials ya reservation form ki details) system mein kahan se aata hai, kahan process hota hai, aur kahan store (database) hota hai.
**Fayda:** Data ka flow samajhne mein asani hoti hai, ki jab user form submit karta hai toh peeche kya process hota hai.

## 3. Sequence Diagram (`SEQUENCE_DIAGRAM.md`)
**Kya kaam ho raha hai?**  
Ismein ek strict step-by-step order dikhaya gaya hai. Jaise, jab Customer "Reserve" button dabata hai, toh pehle Frontend API ko request bhejta hai, API database mein save karti hai, aur wapas Success message deti hai. Uske baad Admin us request ko kaise dekhta hai, yeh bhi time-sequence ke hisaab se samjhaya gaya hai.
**Fayda:** API endpoints aur functions kis sequence mein call hone hain, yeh clear hota hai.

## 4. Workflows (`WORKFLOW.md`)
**Kya kaam ho raha hai?**  
Ismein State Diagrams hain jo Customer aur Admin ke raaste (journeys) ko define karte hain. Customer login karke form fill karta hai aur wapas dashboard par aata hai. Admin login karke approvals deta hai aur menu update karta hai.
**Fayda:** User ki screen-to-screen journey samajh aati hai.

## 5. Entity-Relationship Diagram (`ERD.md`)
**Kya kaam ho raha hai?**  
Yeh database ki collections (Tables) ko dikhata hai — Users, Reservations, aur Menu Items. Aur batata hai ki inmein kya fields (jaise name, email, password) hain aur unka aapas mein kya relation hai.
**Fayda:** Database design aur NoSQL schema ko clearly samajhne ke liye.

## 6. Component Diagram (`COMPONENT_DIAGRAM.md`)
**Kya kaam ho raha hai?**  
Yeh Frontend React app ka breakdown hai. App -> Router -> Navbar, Main Content, Footer. Phir Main Content ke andar alag-alag pages (Home, Menu, Contact) aur unke andar ke chhote components.
**Fayda:** Naye React developers ko samajh aata hai ki kis file aur folder mein kya rakha hai.

## 7. Deployment Diagram (`DEPLOYMENT.md`)
**Kya kaam ho raha hai?**  
Yeh dikhata hai ki aapka code cloud par kahan aur kaise host ho raha hai. Jaise Frontend CDN (Vercel) par hai, Backend server kisi cloud (Render/Heroku) par chal raha hai, aur Database MongoDB Atlas par hai.
**Fayda:** DevOps aur Server Hosting samajhne ke liye.

## 8. Use Case Diagram (`USE_CASE.md`)
**Kya kaam ho raha hai?**  
Yeh simply batata hai ki kon kya kar sakta hai. Admin (Manage Reservations, Edit Menu), Customer (Login, Book Table), aur Guest (View Menu, Register).
**Fayda:** Requirements aur features ko explicitly define karne ke liye.

## 9. Class Diagram (`CLASS_DIAGRAM.md`)
**Kya kaam ho raha hai?**  
Yeh code level par kaam karta hai. Backend controllers aur Data Models (User, Reservation, Menu) ki classes, functions aur properties ko dikhata hai.
**Fayda:** Backend API developers ko OOPs concept samajhne mein madad milti hai.

## 10. State Diagram (`STATE_DIAGRAM.md`)
**Kya kaam ho raha hai?**  
Yeh sirf ek "Table Reservation" ki life cycle batata hai. Ek request pehle 'Pending' hoti hai, fir 'Confirmed' ya 'Rejected' hoti hai, aur end mein 'Completed' ya 'Cancelled'.
**Fayda:** Logic bugs ko avoid karne ke liye status ka clear rulebook mil jata hai.

## 11. Activity Diagram (`ACTIVITY_DIAGRAM.md`)
**Kya kaam ho raha hai?**  
Yeh ek flowchart hai jo decision making batata hai. Jaise: Agar user logged-in hai -> toh Form dikhao -> Varna -> Login page par bhejo.
**Fayda:** Code mein `if-else` conditions kaise likhni hain, iska map mil jata hai.

## 12. Mindmap (`MINDMAP.md`)
**Kya kaam ho raha hai?**  
Yeh project ka ek ped (tree) jaisa visual hai. Isme frontend stack, backend stack, aur features ko points mein tod kar rakha gaya hai.
**Fayda:** Quick project overview kisi meeting ya presentation mein dikhane ke liye.

## 13. Git Branching & Gantt Charts (`GIT_GRAPH.md`, `GANTT_CHART.md` etc.)
**Kya kaam ho raha hai?**  
- **Git Graph**: Code branches (feature branch se main branch mein merge) ka history flow dikhata hai.
- **Gantt Chart**: Project kab shuru hua aur frontend/backend kitne dino mein banega, uska schedule.
- **Network / C4 / Timeline**: Advanced networking, business timelines aur enterprise-level architecture dikhate hain.

---
*Created for Urban Spoon - Development & Documentation*
