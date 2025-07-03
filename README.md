# NotifyNest 🚀

A microservices-based notification delivery system built with **Kafka**, **Node.js**, and **Docker**. Designed to simulate scalable SaaS workflows like billing, email triggers, and audit logging.

## 🧩 Microservices

- `auth-service` – User registration and JWT auth
- `notification-service` – Accepts notification POST and sends Kafka events
- `email-service` – Kafka consumer to process and "send" mock emails
- `audit-service` – Logs every event for monitoring and compliance
- (optional) `dashboard` – Frontend UI to trigger/test notifications

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
