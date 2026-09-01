# ⚙️ Express Basics Cheat Sheet

## 🚀 Quick Start Server
```javascript
const express = require('express');
const app = express();
const PORT = 3000;

app.use(express.json()); // Middleware for parsing JSON bodies

app.get('/', (req, res) => {
  res.send('Hello World!');
});

app.listen(PORT, () => {
  console.log(`Server running on http://localhost:${PORT}`);
});
```

## 🛣️ Routing & Params
| Action | Syntax | Description |
| :--- | :--- | :--- |
| **GET** | `app.get('/path', (req, res) => { ... })` | Retrieve data |
| **POST** | `app.post('/path', (req, res) => { ... })` | Create data |
| **Route Params** | `app.get('/user/:id', ...)` | Access via `req.params.id` |
| **Query Params** | `GET /search?q=term` | Access via `req.query.q` |

## 🛡️ Middleware
Middleware functions have access to the `req`, `res`, and the `next` function.
```javascript
const logger = (req, res, next) => {
  console.log(`${req.method} ${req.url}`);
  next(); // Pass control to next handler
};

app.use(logger);
```

## ⚠️ Error Handling
Always use a global error handler at the end of the middleware stack.
```javascript
app.use((err, req, res, next) => {
  console.error(err.stack);
  res.status(500).send('Something broke!');
});
```
