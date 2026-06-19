# Inventory Management System

A full-stack Inventory Management System designed to manage electrical and mechanical inventory items efficiently.

## Overview

This application provides CRUD operations for inventory items categorized into **Electrical** and **Mechanical** domains while maintaining a history of all inventory updates.

---

# Features

- Add new inventory items
- View all inventory items
- View a single inventory item
- Update inventory details
- Delete inventory items
- Separate Electrical and Mechanical inventory
- Inventory history tracking
- RESTful API architecture
- Modular backend structure

---

# Tech Stack

| Layer | Technology |
|--------|------------|
| Frontend | React |
| Backend | Node.js + Express.js |
| Database | MongoDB |

---

# Project Structure

```
src/
│
├── config/
├── middleware/
├── utils/
│
└── modules/
    │
    ├── electrical/
    │   ├── controllers/
    │   ├── services/
    │   ├── routes/
    │   └── models/
    │
    ├── mechanical/
    │   ├── controllers/
    │   ├── services/
    │   ├── routes/
    │   └── models/
```

---

# API Endpoints

## Electrical Inventory

| Method | Endpoint |
|---------|----------|
| POST | `/api/v1/electrical/items` |
| GET | `/api/v1/electrical/items` |
| GET | `/api/v1/electrical/items/:id` |
| PUT | `/api/v1/electrical/items/:id` |
| DELETE | `/api/v1/electrical/items/:id` |

---

## Mechanical Inventory

| Method | Endpoint |
|---------|----------|
| POST | `/api/v1/mechanical/items` |
| GET | `/api/v1/mechanical/items` |
| GET | `/api/v1/mechanical/items/:id` |
| PUT | `/api/v1/mechanical/items/:id` |
| DELETE | `/api/v1/mechanical/items/:id` |

---

# Inventory Data Model

```
Inventory Item
│
├── Item Information
│   ├── Item ID
│   ├── Item Name
│   ├── Item Type
│   │   ├── Electrical
│   │   └── Mechanical
│   ├── Category
│   ├── Description
│   ├── Quantity
│   ├── Unit
│   ├── Location
│   └── Status
│
├── Creation Information
│   ├── Logged By
│   └── Logged At
│
└── Update Information
    ├── Last Updated By
    └── Last Updated At
```
### Field Description

| Field | Description |
|-------|-------------|
| `itemId` | Unique identifier assigned to each inventory item |
| `itemName` | Name of the inventory item |
| `itemType` | Specifies whether the item belongs to the **Electrical** or **Mechanical** category |
| `category` | Classification of the item (e.g., Motors, Sensors, Fasteners, Cables, Bearings) |
| `description` | Brief description of the inventory item |
| `quantity` | Current available quantity in stock |
| `unit` | Measurement unit (e.g., Pieces, Meters, Kilograms, Liters) |
| `location` | Physical storage location of the item |
| `status` | Current status of the item (Available, Low Stock, Out of Stock, Discontinued, etc.) |
| `loggedBy` | Name of the person who initially added the item |
| `loggedAt` | Date and time when the item was created |
| `lastUpdatedBy` | Name of the person who last modified the item |
| `lastUpdatedAt` | Date and time of the most recent update |

---


# Installation

Clone the repository

```bash
git clone https://github.com/nextup123/inventory_manager.git
```

Move into the project

```bash
cd inventory_manager
```

Install dependencies

```bash
npm install
```

Start the development server

```bash
npm run dev
```

---

# Environment Variables

Create a `.env` file in the project root.

```env
PORT=5000

MONGO_URI=<your-mongodb-connection-string>

NODE_ENV=development
```

---

# Future Improvements

- Authentication & Authorization
- Dashboard Analytics
- Search & Filtering
- Pagination
- Low Stock Alerts

---

# License

This project is licensed under the MIT License.

---
