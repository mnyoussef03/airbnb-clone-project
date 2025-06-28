
# Airbnb Clone Project

## Overview

The Airbnb Clone Project is a full-stack web application inspired by Airbnb. The goal is to develop a scalable platform for property booking that includes user management, property listings, booking systems, payments, and reviews. The project follows modern software engineering practices including version control, CI/CD, and API security.

---

## Team Roles

- **Backend Developer**: Responsible for building and maintaining the backend logic, REST/GraphQL APIs, and managing server-side integration.
- **Database Administrator**: Designs, manages, and optimizes the database schema and queries to ensure data integrity and performance.
- **DevOps Engineer**: Sets up and manages CI/CD pipelines, deployment processes, and server infrastructure (using Docker, GitHub Actions, etc.).
- **Product Manager**: Coordinates team efforts, plans features, ensures deadlines are met, and aligns the product with business goals.

---

## Technology Stack

- **Django**: A Python web framework used for building the backend logic and APIs.
- **MySQL**: Relational database system used to store users, bookings, properties, etc.
- **GraphQL**: API query language for flexible and efficient data retrieval.
- **Docker**: Used to containerize the application for consistent development and deployment environments.
- **GitHub Actions**: Tool for automating workflows like testing, building, and deployment.

---

## Database Design

### Entities and Fields:

- **User**: `id`, `name`, `email`, `password`
- **Property**: `id`, `user_id`, `title`, `location`, `price`
- **Booking**: `id`, `user_id`, `property_id`, `start_date`, `end_date`
- **Review**: `id`, `user_id`, `property_id`, `rating`, `comment`
- **Payment**: `id`, `booking_id`, `amount`, `payment_status`, `timestamp`

### Relationships:

- A **User** can own multiple **Properties**.
- A **Booking** is linked to both a **User** and a **Property**.
- A **Review** is linked to a **User** and a **Property**.
- A **Payment** is associated with a **Booking**.

---

## Feature Breakdown

- **User Management**: Users can register, log in, update their profile, and manage their bookings.
- **Property Management**: Hosts can create, edit, and delete their property listings with details and availability.
- **Booking System**: Users can browse properties, check availability, and make bookings with start and end dates.
- **Review System**: After staying at a property, users can leave a rating and a written review.
- **Payment Handling**: Secure payment processing for each booking, with transaction history for users and hosts.

---

## API Security

- **Authentication**: Users must log in via token-based authentication (e.g., JWT) to access personal and booking data.
- **Authorization**: Only authorized users can manage their own listings, bookings, or payments.
- **Rate Limiting**: Throttling mechanisms to prevent abuse (e.g., too many login attempts).
- **Input Validation**: Every user input is validated to prevent SQL injection and XSS attacks.

> Security is essential for protecting user data, ensuring safe financial transactions, and maintaining the integrity of the platform.

---

## CI/CD Pipeline

- **Continuous Integration (CI)**: Automatically tests and validates every code push to avoid breaking features.
- **Continuous Deployment (CD)**: Deploys the application automatically to staging or production when tests pass.

### Tools Used:

- **GitHub Actions**: Automates testing, building, and deployment workflows.
- **Docker**: Packages the app with its environment so it works everywhere identically.
- **(Optional)**: Services like Heroku, Render, or AWS for deployment.

---

## License

This project is for educational purposes only.


