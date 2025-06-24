```markdown
# 📦 Product API – Express.js RESTful Assignment

This project is a simple RESTful API built using **Express.js** for managing products. It demonstrates routing, middleware, authentication, error handling, filtering, pagination, and search.

---

## 🚀 Getting Started

### 🔧 Prerequisites

- Node.js (v18+)
- npm

### 📥 Installation

1. Clone your repository:
   ```bash
   git clone <your-assignment-repo-url>
   cd week-2-express-js-assignment-francis-auka
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the server:
   ```bash
   npm start
   ```

4. Open in browser:
   ```
   http://localhost:8080/
   ```

---

## 🔐 Authentication

Some endpoints require a simple `Authorization` header:

```
Authorization: Bearer secret
```

---

## 📚 API Endpoints

### ➤ `GET /api/products`

Retrieve all products. Supports search, pagination, and filtering.

#### Optional query parameters:

| Param    | Type   | Description                      |
|----------|--------|----------------------------------|
| `search` | string | Search by product name           |
| `page`   | number | Page number (default: 1)         |
| `limit`  | number | Items per page (default: 10)     |

#### Example:
```
GET /api/products?search=phone&page=1&limit=2
```

---

### ➤ `GET /api/products/:id`

Get a specific product by its ID.

#### Example:
```
GET /api/products/1
```

---

### ➤ `POST /api/products` 🔒

Create a new product.

#### Headers:
```
Authorization: Bearer secret
Content-Type: application/json
```

#### Body:
```json
{
  "name": "Keyboard",
  "description": "Mechanical keyboard",
  "price": 150,
  "category": "electronics",
  "inStock": true
}
```

---

### ➤ `PUT /api/products/:id` 🔒

Update an existing product.

#### Headers:
```
Authorization: Bearer secret
Content-Type: application/json
```

#### Body (example):
```json
{
  "price": 120
}
```

---

### ➤ `DELETE /api/products/:id` 🔒

Delete a product by its ID.

#### Headers:
```
Authorization: Bearer secret
```

---

## 🛠 Middleware Features

- ✅ Request logging
- ✅ Basic authentication (`Bearer secret`)
- ✅ Centralized error handling

---

## 📂 In-Memory Data

This API uses a temporary array of product objects stored in-memory (no database). Restarting the server will reset the data.

---

## ✍️ Author

**Francis Auka**  
Assignment for **Week 2 – Express.js RESTful API**  
PLPACADEMY

---

## ✅ Status

✔️ All features implemented and tested  
✔️ Ready for submission via GitHub Classroom
```
