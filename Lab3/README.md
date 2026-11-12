
# Lab 3 – Software Architecture and UML Component Diagram

**Course:** Software Engineering  
**Student:** Srijan Kumar  
**SRN:** PES1UG24CS467  
**Problem Statement:** #36 – Restaurant Table Booking & Pre-Ordering App

## 1. Project Overview

This lab documents the software architecture of a restaurant table booking and pre-ordering application. The system allows diners to select tables, make reservations, place advance food orders, and supports restaurant staff in managing reservations and kitchen preparation.

## 2. Architectural Style

**Selected Architecture: Layered Architecture**

The system is organised into presentation, business-logic, and data-access responsibilities. This separation keeps user interaction, application processing, and data storage concerns distinct.

The layered approach is suitable for this application because:

- It separates diner and manager interfaces from reservation, ordering, and payment processing.
- It provides a clear structure that is straightforward to maintain and extend as the application grows.

## 3. Main Components

The component diagram represents the following five components:

1. **Diner / Manager Interface** – Provides user-facing functions for diners and restaurant managers.
2. **Order Manager** – Coordinates reservations and pre-orders and manages the order workflow.
3. **Payment Service** – Handles payment processing requests.
4. **Table and Menu Service** – Supports table availability, table selection, and menu information.
5. **Kitchen / Receipt Service** – Receives order information for kitchen preparation and receipt-related processing.

## 4. Component Interactions

The diagram shows communication between the components, including:

- The Diner / Manager Interface communicates user actions to the Order Manager.
- The Order Manager requests table and menu information from the Table and Menu Service.
- The Order Manager communicates with the Payment Service to process payment requests.
- The Order Manager passes confirmed order information to the Kitchen / Receipt Service.

The Order Manager and Payment Service interaction is specifically required by the lab handout. Interfaces and dependencies are represented in the component diagram.

## 5. Security and Performance Considerations

The layered design supports security by keeping application processing separate from the user interface, allowing authentication and authorization checks to be applied in the application layer. Secure communication such as HTTPS/TLS can protect information transmitted between clients and services.

Separating responsibilities also helps performance tuning. Frequently requested table availability and menu information can be handled efficiently, while reservation and order processing remain organised within the business-logic layer.

## 6. Deliverables

| File | Description |
|---|---|
| Component_Diagram.pdf | UML component diagram showing the system components and their interactions. |
| Architecture_Justification.pdf | Written justification of the selected architecture, including scenario-related reasons, security, and performance considerations. |

## 7. Repository Structure

```text
Lab-1-Requirements-Engineering/
└── Lab3/
    ├── README.md
    ├── Component_Diagram.pdf
    └── Architecture_Justification.pdf
```

## 8. Tools Used

- draw.io – UML component diagram creation
- Microsoft Word – Architecture justification
- GitHub – Version control and submission of Lab 3 deliverables
