# Food-Ordering-Application
A scalable Spring Boot based food ordering service implementing DDD, Clean Architecture, SAGA, CQRS, Outbox, and Kafka. I followed a [course](https://www.udemy.com/course/microservices-clean-architecture-ddd-saga-outbox-kafka-kubernetes/) on udemy for this project.

![General Diagram of the Application](./images/FoodOrderingApplication.png)

**Hexagonal Architecture:** Hexagonal Architecture, also known as the Ports and Adapters pattern, is a software design approach that separates the core business logic from external systems such as databases, APIs, and user interfaces.

The core domain sits in the center and communicates with the outside world through ports (interfaces) and adapters (implementations). This allows the application to be easily tested, replaced, or extended without affecting the business logic. It improves maintainability, flexibility, and independence from infrastructure details.

![General Diagram of the Hexagonal Architecture](./images/HexagonalArch.png)

Clean Architecture is used with Hexagonal Architecture interchangebly. Comparison of clean and layered architecture is below:

![Comparison of the Architecture](./images/Layered_vs_Clean.png)

## 1. Order Service

Order service is designed by tactical domain driven development. Aggregates, value objects and event and the hierarchy is depicted in the figure from course:

![Order Service DDD](./images/order-service-domain-logic-oncourse.png)

### Order States
Order states are determined as {*PENDING*, *PAID*, *APPROVED*, *CANCELLING*, *CANCELLED*}. The state changes can be showed in the figure below from course:

![Order State Changes](./images/order-state-transitions.png)