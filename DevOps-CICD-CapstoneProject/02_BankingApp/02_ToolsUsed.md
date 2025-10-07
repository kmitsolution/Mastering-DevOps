# Project Details: Banking Application & Microservices

## Overview

This repository contains a professional Banking Application frontend and four backend microservices. The frontend is a single HTML page that interacts with the microservices using HTTP requests.

## Components

### 1. Frontend

- **File:** `index.html`
- **Description:**  
  The main page for the Banking Application. It features a banking logo, four buttons to access different services, and displays responses from the backend.
- **Technologies:**  
  - HTML, CSS, JavaScript
  - Designed and edited in Visual Studio Code

### 2. Backend Microservices

Each service is a separate Java Spring Boot project managed with Maven:

| Service           | Endpoint URL                              | Port  |
|-------------------|-------------------------------------------|-------|
| Internet Banking  | http://localhost:8080/internet-banking    | 8080  |
| Withdraw          | http://localhost:8081/withdraw            | 8081  |
| Deposit           | http://localhost:8082/deposit             | 8082  |
| Customer Care     | http://localhost:8083/customer-care       | 8083  |

- **Description:**  
  Each microservice exposes a GET endpoint that returns a message indicating the service was called.
- **Technologies:**  
  - Java
  - Spring Boot
  - Maven

## How It Works

- The user interacts with the Banking Application via the main page (`index.html`).
- Clicking a button sends a GET request to the corresponding microservice.
- The microservice responds with a confirmation message, which is displayed on the page.

## Development Tools

- **Visual Studio Code:** Used for editing and managing all project files.
- **Spring Boot:** Framework for building Java microservices.
- **Maven:** Dependency and build management for Java projects.

## Additional Notes

- Ensure all microservices are running on their respective ports before using the frontend.
- CORS is enabled on all microservices to allow browser-based requests.
- The banking logo should be placed in the `images` folder as `bank-logo.png`.

---

© 2025 KMIT Solutions Services. All rights reserved.
