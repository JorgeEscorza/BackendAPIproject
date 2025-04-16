# Invoice API - Backend Web Development Project

This repository contains a backend web development project.

## 📋 Project Overview

The purpose of this project is to show the development of a **Spring Boot API** for managing client invoices based on selected products. The API supports shopping cart operations, validation of product availability, and generation of complete invoices with tax calculations (I've done another API to manage exchange-rate, but maybe I'll upload it in another repository).

This API is integrated into a **microservices architecture** that includes:
- `customer-service`
- `product-service`
- `invoice-service` (this project)
- `config-service` (centralized config)
- `eureka-server` (service registry)
- `admin-service` (monitoring)
- `gateway-service` (API gateway)

---

## ✅ Main Features

- **Add to Cart**: Validates customer RFC and checks if the product exists via GTIN. It verifies stock availability before adding or updating items in the cart.
- **Update Quantity**: If a product already exists in the cart, it updates the quantity rather than duplicating the entry.
- **Generate Invoice**:
  - Calculates total, subtotal, and taxes (16% IVA).
  - Updates product stock.
  - Stores all invoice and item data in the database.
  - Empties the customer's cart once the invoice is generated.

And so on!

---

## ⚙️ Technologies Used

- Java 11
- Spring Boot 2.7.10
- Maven
- Eureka Server
- Spring Cloud Gateway
- Spring Config Server
- Spring Admin Server
- REST APIs
- MySQL
- Postman

---

## 🧪 Example Validations

- Adding a product that exceeds stock → ❌ `"invalid quantity"`
- Adding a non-existent product → ❌ `"product does not exist"`
- Generating an invoice from an empty cart → ❌ `"cart has no items"`
- Successful invoice generation → ✅ returns invoice with tax breakdown

---

## 🤝 Connect

Feel free to connect with me on [LinkedIn](https://www.linkedin.com/in/jorge-luis-escorza-s%C3%A1nchez-9ab935325/) for collaboration, questions, or just to say hi!
