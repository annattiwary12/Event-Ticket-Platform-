# 🎟️ Event-Ticket-Platform

A full-stack Event Ticket Management Platform that allows organizers to create events, attendees to purchase tickets, and staff to validate tickets using QR codes.

This platform manages the complete event lifecycle — from event creation to ticket sales, real-time reporting, and on-site ticket validation.

------------------------------------------------------------
🚀 Tech Stack
------------------------------------------------------------

Backend:
- Java 21
- Spring Boot 3
- Spring Security
- OAuth2 Resource Server
- PostgreSQL
- Spring Data JPA
- MapStruct
- Lombok
- Docker

Frontend:
- React
- Vite

Authentication:
- Keycloak (OAuth2 + OpenID Connect)

------------------------------------------------------------
🏗️ Architecture Overview
------------------------------------------------------------

React Frontend  --->  Spring Boot REST API  --->  PostgreSQL
        |                       |
        |                       |
        --------> Keycloak <-----

- React handles UI
- Spring Boot exposes REST APIs
- PostgreSQL stores data
- Keycloak manages authentication & roles
- Docker runs local infrastructure

------------------------------------------------------------
👥 User Roles
------------------------------------------------------------

Organizer:
- Create and manage events
- Configure ticket types and pricing
- Monitor sales dashboard
- Generate reports

Attendee:
- Browse published events
- Purchase tickets
- Receive QR code tickets
- View purchased tickets

Staff:
- Scan QR codes
- Validate tickets
- Prevent duplicate entry
- Monitor entry flow

------------------------------------------------------------
📦 Domain Model
------------------------------------------------------------

Core Entities:
- User
- Event
- TicketType
- Ticket
- TicketValidation
- QrCode

Event Status:
- DRAFT
- PUBLISHED
- CANCELLED
- COMPLETED

Ticket Status:
- PURCHASED
- CANCELLED

Ticket Validation:
- VALID
- INVALID
- EXPIRED

------------------------------------------------------------
🔌 REST API (Sample Endpoints)
------------------------------------------------------------

Event Management:
POST   /api/v1/events
GET    /api/v1/events
GET    /api/v1/events/{id}
PUT    /api/v1/events/{id}
DELETE /api/v1/events/{id}

Ticket Purchase:
GET    /api/v1/published-events
POST   /api/v1/published-events/{id}/ticket-types/{ticketTypeId}

Ticket Validation:
POST   /api/v1/events/{eventId}/ticket-validations

------------------------------------------------------------
⚙️ Local Setup (Docker Required)
------------------------------------------------------------

1. Clone Repository

git clone https://github.com/your-username/Event-Ticket-Platform.git
cd Event-Ticket-Platform

2. Start Infrastructure

docker-compose up

Services:
- PostgreSQL (Port 5432)
- Adminer (Port 8888)
- Keycloak (Port 9090)

3. Run Backend

./mvnw spring-boot:run

4. Run Frontend

cd frontend
npm install
npm run dev

------------------------------------------------------------
🔐 Keycloak Configuration
------------------------------------------------------------

Realm: event-ticket-platform
Client ID: event-ticket-platform-app
Redirect URI: http://localhost:5173
Issuer URI:
http://localhost:9090/realms/event-ticket-platform

------------------------------------------------------------
📊 Features
------------------------------------------------------------

✔ Event Creation & Management  
✔ Multiple Ticket Types  
✔ Secure OAuth2 Authentication  
✔ Real-Time Ticket Inventory  
✔ QR Code Generation  
✔ Ticket Validation System  
✔ Sales Reporting  
✔ Role-Based Access Control  

------------------------------------------------------------
🧪 Testing
------------------------------------------------------------

- H2 database used for testing
- Spring Boot Test
- Spring Security Test

------------------------------------------------------------
📄 License
------------------------------------------------------------

This project is built for educational purposes.
You may adapt and extend it for learning and portfolio use.

------------------------------------------------------------
👨‍💻 Author
------------------------------------------------------------

<img width="946" height="478" alt="image" src="https://github.com/user-attachments/assets/6f9a3536-7e20-4eea-9d31-7ce19bf4ae4a" />
