# 🚀 Notification Service

A robust and scalable backend microservice built with **Spring Boot** that handles user notifications via **Email**, **SMS**, and **In-App** alerts.

---

## 📌 Key Features

- Send notifications via:
  - 📧 Email
  - 📱 SMS
  - 🔔 In-App
- RESTful API endpoints
- Asynchronous processing with **RabbitMQ**
- Retry mechanism for failed notifications
- Extensible architecture for adding more notification types

---

## 🛠️ Tech Stack

- **Java 17**
- **Spring Boot 3.x**
- **Spring Data JPA**
- **Spring Mail**
- **RabbitMQ** (Optional)
- **H2 / PostgreSQL** (Configurable)
- **Lombok**
- **Maven**

---

## 📂 Project Structure
```
src/
├── main/
│ ├── java/
│ │ └── com/yourcompany/notification
│ │ ├── controller/
│ │ ├── service/
│ │ ├── repository/
│ │ ├── model/
│ │ ├── dto/
│ │ └── config/
│ └── resources/
│ ├── application.properties
│ └── templates/
```
---

## 🚀 Getting Started

### Prerequisites

- Java 17+
- Maven 3.x
- RabbitMQ (optional, for async mode)

### Steps

```bash
# 1. Clone the repo
git clone https://github.com/Arpreet2107/PepSales-assignment.git
cd notification-service

# 2. Build the project
mvn clean install

# 3. Run the application
mvn spring-boot:run

The server will start at:
http://localhost:8080
```
### 📬 API Endpoints
```POST /notifications
Send a new notification.

json
Copy
Edit
{
"userId": "1",
"type": "EMAIL | SMS | IN_APP",
"message": "Hello from the notification service!"
}
```
### GET /users/{userId}/notifications
```
Retrieve all notifications sent to a specific user.

🧠 Assumptions & Notes
Email is configured using SMTP credentials in application.properties.

SMS integration is mocked (plug in Twilio or other providers).

In-App notifications are persisted and queryable.

RabbitMQ queue support is optional and can be enabled via configuration.
```
### 💡 Future Enhancements
```Notification templates

Admin dashboard for analytics

Kafka-based event streaming

Multi-language support
```

### 👨‍💻 Author
```
Arpreet Mahala
```
