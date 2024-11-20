
# Golang REST Server

This is a simple REST server built using the [Fiber](https://gofiber.io/) web framework in Golang. It provides a basic **To-Do List API** with endpoints to create, retrieve, update, and delete tasks.

---

## **Installation**

1. Clone the repository:
   ```bash
   git clone https://github.com/Lingesh15/Golang-REST-Server.git
   ```
2. Navigate to the project directory:
   ```bash
   cd Golang-REST-Server
   ```
3. Install dependencies:
   ```bash
   go mod tidy
   ```
4. Run the server:
   ```bash
   go run main.go
   ```

By default, the server runs on `http://localhost:3000`.

---

## **API Endpoints**

### **1. Get All To-Do Items**
**Endpoint**: `GET /api/todos`

**cURL Command**:
```bash
curl -X GET http://localhost:3000/api/todos
```

**Response**:
```json
[
    {
        "id": 1,
        "body": "First todo",
        "completed": false
    }
]
```

---

### **2. Create a To-Do Item**
**Endpoint**: `POST /api/todos`

**cURL Command**:
```bash
curl -X POST http://localhost:3000/api/todos -H "Content-Type: application/json" -d "{\"body\": \"This is my todo\"}"
```

**Response**:
```json
{
    "id": 1,
    "body": "This is my todo",
    "completed": false
}
```

---

### **3. Update a To-Do Item (Mark as Completed)**
**Endpoint**: `PUT /api/todos/:id`

**cURL Command**:
```bash
curl -X PUT http://localhost:3000/api/todos/1 -H "Content-Type: application/json"
```

**Response**:
```json
{
    "id": 1,
    "body": "This is my todo",
    "completed": true
}
```

---

### **4. Delete a To-Do Item**
**Endpoint**: `DELETE /api/todos/delete/:id`

**cURL Command**:
```bash
curl -X DELETE http://localhost:3000/api/todos/delete/1 -H "Content-Type: application/json"
```

**Response**:
```json
{
    "message": "Todo deleted successfully"
}
```

---

## **Project Structure**
```
.
├── main.go      # Entry point for the server
├── go.mod       # Module file for dependencies
├── go.sum       # Checksum file for dependencies
└── README.md    # Documentation
```

---




