# Ecommerce-web-app
This project presents a full-stack E-Commerce Web Application built with Spring Boot, Spring Data JPA, and MySQL, exposing REST APIs consumed by a Bootstrap-styled frontend. Users can browse products, add to cart, and place orders; admins can manage products and orders. The app implements role-based authentication and a layered architecture for maintainability and scalability.

Introduction

The application demonstrates a secure, modular, and scalable online shopping system. It includes user-facing flows (catalogue, cart, checkout) and administrative capabilities (product CRUD, order visibility). The stack leverages Java Spring Boot for the backend and a relational database for persistence.

Objectives

Implement secure authentication/authorization (User/Admin).

Provide product browsing, search, and sorting.

Enable cart and order placement with totals.

Offer an Admin dashboard for product and order management.

Use REST APIs to decouple frontend and backend.

Methodology
Architecture

Frontend: HTML, CSS, JavaScript, Bootstrap (responsive UI).

Backend: Spring Boot (Controllers → Services → Repositories).

Persistence: Spring Data JPA (Hibernate) with MySQL.

Security: Spring Security with role-based access control.

Build/Run: Maven, application properties for DB credentials.

Layers

Presentation: Controllers/Views (Bootstrap UI).

Business Logic: Services (validation, orchestration).

Data Access: JPA Repositories.

Database: MySQL schema with normalized entities.

Implementation
Key Features

User registration/login with encrypted passwords.

Product catalogue with category and sort filters.

Cart operations: add/remove/update quantity, compute totals.

Checkout and order confirmation.

Admin module for product CRUD and order overview.

Example Database Schema

users(id, name, email, password_hash, role)

products(id, name, description, category, price, stock)

carts(id, user_id) / cart_items(id, cart_id, product_id, quantity)

orders(id, user_id, order_date, status, total)

order_items(id, order_id, product_id, quantity, price)

Core Endpoints (Illustrative)

POST /auth/register, POST /auth/login

GET /products, GET /products/{id}

POST /cart/items, PUT /cart/items/{id}, DELETE /cart/items/{id}

POST /orders, GET /orders/{id}

Admin: POST/PUT/DELETE /admin/products, GET /admin/orders

Results

The application runs on http://localhost:8080 with the following user-visible pages:

Login

Product Catalogue

Cart & Order Summary

Order Confirmation

Admin Dashboard (Products)
