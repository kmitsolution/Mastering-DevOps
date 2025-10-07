# Banking Application Project Overview

## Introduction

This project is a demonstration of a **Banking Application** that interacts with multiple backend microservices. The frontend is a simple HTML/CSS/JavaScript page, while the backend consists of four independent Java Spring Boot microservices, each built using Maven.

<img width="397" height="416" alt="image" src="https://github.com/user-attachments/assets/d89f40a0-24d9-4bfb-94ea-09633c5ba3b4" />

## Architecture

- **Frontend:**  
  - `index.html` provides a user interface with four buttons.
  - Each button calls a specific microservice via HTTP GET requests.
  - The responses from the microservices are displayed on the page.

- **Backend Microservices:**  
  Each microservice is a standalone Spring Boot application:
  1. **Internet Banking Service**  
     - URL: `http://localhost:8080/internet-banking`
  2. **Withdraw Service**  
     - URL: `http://localhost:8081/withdraw`
  3. **Deposit Service**  
     - URL: `http://localhost:8082/deposit`
  4. **Customer Care Service**  
     - URL: `http://localhost:8083/customer-care`

## How It Works

- When a user clicks a button on the Banking Application page, a JavaScript function sends a GET request to the corresponding microservice.
- Each microservice responds with a simple message indicating its service was called (e.g., "Internet Banking service is called").
- The frontend displays the response to the user.

## Technologies Used

- **Frontend:** HTML, CSS, JavaScript
- **Backend:** Java, Spring Boot, Maven

## Running the Project

1. Start each microservice on its respective port.
2. Open `index.html` in a browser.
3. Click any button to interact with the microservices.

## Microservice Endpoints

| Service           | URL                                 | Port  |
|-------------------|-------------------------------------|-------|
| Internet Banking  | http://localhost:8080/internet-banking | 8080  |
| Withdraw          | http://localhost:8081/withdraw         | 8081  |
| Deposit           | http://localhost:8082/deposit          | 8082  |
| Customer Care     | http://localhost:8083/customer-care    | 8083  |

## Notes

- Ensure all microservices are running before using the frontend.
- CORS is enabled on all microservices to allow browser requests.

---
© 2025 KMIT Solutions Services. All rights reserved.
