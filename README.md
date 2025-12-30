# NotifyNest 🚀

A microservices-based notification delivery system built with **Kafka**, **Node.js**, and **Docker**. Designed to simulate scalable SaaS workflows like billing, email triggers, and audit logging.

## 🛠 Stack

- Node.js, Express.js
- Kafka + KafkaJS
- MongoDB (audit logs)
- Docker + Docker Compose

## 📦 Architecture

```mermaid
graph TD;
    User-->NotificationService
    NotificationService-->Kafka
    Kafka-->EmailService
    Kafka-->AuditService
