# 📄 Requirement Specifications – Airbnb Clone Backend

This document outlines the technical and functional requirements for core backend features in the Airbnb Clone project.

---

## 🔐 Feature 1: User Authentication

### API Endpoints

- `POST /api/register`
- `POST /api/login`
- `GET /api/profile`

### Inputs

- Registration: name, email, password
- Login: email, password

### Outputs

- JWT token, success/error response

### Validation

- Unique email
- Password length >= 8
- Email format check

### Performance

- Response within 200ms
- Token validity: 7 days

---

## 🏠 Feature 2: Property Management

### API Endpoints

- `POST /api/properties`
- `PUT /api/properties/:id`
- `DELETE /api/properties/:id`
- `GET /api/properties`

### Inputs

- Title, description, location, price, availability

### Outputs

- Property object, success message

### Validation

- Title max length: 150 chars
- Price must be a positive decimal

### Performance

- Query response under 300ms

---

## 📅 Feature 3: Booking System

### API Endpoints

- `POST /api/bookings`
- `GET /api/bookings/:userId`
- `DELETE /api/bookings/:id`

### Inputs

- Property ID, user ID, start_date, end_date

### Outputs

- Booking ID, status, total price

### Validation

- No overlapping bookings
- Start date must be < end date

### Performance

- Booking creation under 500ms
