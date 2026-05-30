🚀 Realtime Notification System

A full-stack realtime notification system built using **Spring Boot, PostgreSQL, WebSocket, STOMP, and SockJS**. The application enables instant user-specific notifications without requiring page refreshes, providing seamless realtime communication between connected clients.


📖 Project Overview

The Realtime Notification System is a full-stack web application that enables instant user-specific notifications using WebSocket communication. Unlike traditional polling mechanisms, notifications are pushed directly from the server to connected clients, ensuring low latency and an enhanced user experience. The system demonstrates real-time messaging, database persistence, and full-stack integration using Spring Boot and PostgreSQL.


✨ Features

* 🔔 Realtime notifications using WebSocket
* 👤 User-specific message delivery
* 🗄️ PostgreSQL database integration
* ⚡ STOMP messaging protocol
* 🔄 SockJS fallback support
* 🌐 Dynamic frontend using HTML, CSS, and JavaScript
* 🚀 Instant UI updates without page refresh
* 🏗️ Layered Spring Boot architecture


🛠️ Tech Stack

| Technology          | Purpose                |
| ------------------- | ---------------------- |
| Java                | Programming Language   |
| Spring Boot         | Backend Framework      |
| PostgreSQL          | Database               |
| WebSocket           | Realtime Communication |
| STOMP               | Messaging Protocol     |
| SockJS              | WebSocket Fallback     |
| HTML/CSS/JavaScript | Frontend               |
| Maven               | Dependency Management  |


🏗️ Architecture

```text
Browser Client
      │
      ▼
Spring Boot REST API
      │
      ▼
Service Layer
      │
      ▼
PostgreSQL Database
      │
      ▼
WebSocket + STOMP
      │
      ▼
Target User Receives Notification
```


🔄 Notification Flow

```text
User Sends Notification
          │
          ▼
REST Controller
          │
          ▼
Service Layer
          │
          ▼
Save Notification in PostgreSQL
          │
          ▼
Publish via WebSocket + STOMP
          │
          ▼
Target User Subscription
          │
          ▼
Notification Appears Instantly
```


📂 Project Structure

```text
config/        → WebSocket Configuration
controller/    → REST & WebSocket Controllers
service/       → Business Logic
repository/    → Database Operations
entity/        → Database Models
dto/           → Data Transfer Objects
static/        → Frontend Files
```


⚙️ How To Run

Clone Repository

```bash
git clone <repository-url>
cd notification_system
```

Configure PostgreSQL

Update the following properties in `application.properties`:

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/notification_db
spring.datasource.username=postgres
spring.datasource.password=your_password
spring.jpa.hibernate.ddl-auto=update
```

Run the Application

```bash
./mvnw spring-boot:run
```

Open in Browser

```text
http://localhost:8081
```


🧪 Realtime Testing

1. Open two browser windows.
2. Connect User 1 and User 2.
3. Send a notification from User 1 to User 2.
4. User 2 receives the notification instantly.
5. No page refresh is required.

Example

**User 1**

```text
Current User ID: 1
Target User ID: 2
Message: Hello User 2
```

**Expected Result**

```text
User 2 instantly receives:
"Hello User 2"
```


📡 WebSocket Endpoint

```text
/ws
```

Topic Subscription

```text
/topic/notifications/{userId}
```

Example:

```text
/topic/notifications/2
```

Only User 2 receives messages published to this topic.


📚 Concepts Covered

* Spring Boot REST APIs
* JPA & Hibernate
* PostgreSQL Integration
* WebSocket Communication
* STOMP Messaging
* User-Specific Notifications
* Realtime Frontend Updates
* Full-Stack Application Development


🔮 Future Enhancements

* Authentication & Authorization
* Read/Unread Notifications
* Toast Popup Notifications
* Message History
* Online/Offline User Tracking
* PostgreSQL LISTEN / NOTIFY
* Redis Message Broker Integration


👨‍💻 Author

Sania Reang

B.Tech CSE Student

Java | Spring Boot | PostgreSQL

