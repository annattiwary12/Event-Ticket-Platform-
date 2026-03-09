# 🎟️ Event Ticket Platform

A backend application for managing events and ticket purchases built with Spring Boot.

Users can browse events, purchase tickets, and validate tickets using QR codes.

This project demonstrates real-world backend architecture, REST API design, authentication, and ticket validation workflows.

--------------------------------------------------

## 🚀 Features

### Event Management
Organizers (staff users) can:

- Create events
- Update event details
- Delete events
- Publish events
- Search events
- List available events

Each event contains:

- Title
- Description
- Location
- Event date
- Ticket types
- Pricing

--------------------------------------------------
<img width="1914" height="891" alt="Screenshot 2026-03-09 115617" src="https://github.com/user-attachments/assets/6fe34c39-9fb2-444c-9bc5-239bea90c6d4" />

### Ticket Purchase System

Attendees can:

- Browse events
- Purchase tickets
- Receive QR code tickets

Ticket purchase flow:

1. User selects an event
2. Selects ticket type
3. Ticket is created in database
4. QR code is generated
5. Ticket is linked to the user

--------------------------------------------------

### QR Code Ticket Validation

At the event venue:

- Staff scans the QR code
- System validates the ticket
- Ticket status becomes VALIDATED

This prevents duplicate entry and ticket fraud.
<img width="1608" height="823" alt="Screenshot 2026-03-09 115552" src="https://github.com/user-attachments/assets/2e3f0b33-e217-4ef9-a555-170fc4e8e6d3" />

--------------------------------------------------

## 👥 User Roles

### Attendee

Can:

- View events
- Purchase tickets
- View purchased tickets
- Access QR code

### Staff

Can:

- Create events
- Manage events
- Validate tickets

--------------------------------------------------
<img width="946" height="478" alt="Screenshot 2026-02-19 000522" src="https://github.com/user-attachments/assets/5736029b-adde-4abc-a19c-9eee17b14c2d" />

## 🏗 Architecture

Controller Layer  
↓  
Service Layer  
↓  
Repository Layer  
↓  
Database  

Controller  
Handles REST API requests and responses.

Service  
Contains business logic such as ticket purchasing and event validation.

Repository  
Handles database interaction using Spring Data JPA.

--------------------------------------------------

## 🧱 Tech Stack

Backend
- Java
- Spring Boot
- Spring Security
- Spring Data JPA

Database
- PostgreSQL

Authentication
- Keycloak

Mapping
- MapStruct

Other Tools
- Docker
- QR Code Generator

--------------------------------------------------

## 📡 API Endpoints

Create Event

POST /events

List Events

GET /events

Purchase Ticket

POST /tickets/purchase

Validate Ticket

POST /tickets/validate

--------------------------------------------------

## ⚙️ Project Setup

Requirements

- Java 17+
- PostgreSQL
- Docker
- Keycloak

Run the project

mvn spring-boot:run

--------------------------------------------------

## 🎯 Learning Outcomes

This project demonstrates:

- Domain modeling
- REST API design
- Spring Security
- OAuth authentication with Keycloak
- DTO and MapStruct usage
- Clean backend architecture
- Ticket purchasing system
- QR code ticket validation
