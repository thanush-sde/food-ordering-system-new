🍔 Food Ordering System

A full-stack food ordering platform with role-based access for customers and restaurant owners. Customers can browse restaurants, order food, and track deliveries. Restaurant owners can manage their menu and fulfill incoming orders.

Tech Stack

Backend: Java 21 · Spring Boot 3.5 · Spring Security · Spring Data JPA (Hibernate) · MySQL · JWT · Maven Frontend: React 19 · Vite · React Router · Tailwind CSS v4 · Axios · Context API

Features
Customer
Register / login with JWT authentication
Browse and search restaurants by name or category
View restaurant menus
Add items to cart and check out
Save and manage delivery addresses
Track order status in real time
Leave reviews for restaurants ordered from
Restaurant Owner
Manage restaurant profile
Add, edit, and manage menu items
View and update incoming order statuses
Architecture
User ──< Role (many-to-many)
User ──< Address
User (owner) ──< Restaurant ──< MenuItem
User (customer) ──< Order ──< OrderItem >── MenuItem
Restaurant ──< Review >── User
Entities

User, Role, Address, Restaurant, MenuItem, Order, OrderItem, Review

Getting Started
Backend
bash
cd backend
# set DB_PASSWORD and JWT_SECRET as environment variables
./mvnw spring-boot:run

Runs on http://localhost:8080.

Frontend
bash
cd frontend
npm install
npm run dev

Runs on http://localhost:5173.