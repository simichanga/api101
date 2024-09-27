# FastAPI CRUD Example

This is a simple FastAPI project demonstrating basic CRUD (Create, Read, Update, Delete) operations using an in-memory database.

## Prerequisites

- Python 3.7 or higher
- FastAPI
- Uvicorn (ASGI server)

## Installation

Clone the repository (or create your own project with the files provided here).

Install the dependencies:

``` bash
    pip install fastapi uvicorn
```

## Running the Application

Run the FastAPI application using Uvicorn:

``` bash
    uvicorn main:app --reload
```
This will start the application on http://127.0.0.1:8000.

Access the API documentation:

FastAPI automatically generates interactive API documentation. You can access it at:
- Swagger UI: http://127.0.0.1:8000/docs
- ReDoc: http://127.0.0.1:8000/redoc

## API Endpoints
### 1. Get All Items

Retrieve a list of all items.

```bash
curl -X GET "http://127.0.0.1:8000/items" -H "accept: application/json"
```

### 2. Create a New Item

Create a new item by sending a POST request with a JSON body.

```bash
curl -X POST "http://127.0.0.1:8000/items" -H "Content-Type: application/json" -d '{
  "id": 1,
  "name": "Laptop",
  "description": "A high-performance laptop",
  "price": 1200.00
}'
```

### 3. Get an Item by ID

Retrieve a specific item by its id.

```bash
curl -X GET "http://127.0.0.1:8000/items/1" -H "accept: application/json"
```

### 4. Update an Item

Update an existing item by sending a PUT request with updated item data in JSON format.

```bash
curl -X PUT "http://127.0.0.1:8000/items/1" -H "Content-Type: application/json" -d '{
  "id": 1,
  "name": "Gaming Laptop",
  "description": "A high-performance gaming laptop",
  "price": 1500.00
}'
```

### 5. Delete an Item

Delete a specific item by its id.

```bash
curl -X DELETE "http://127.0.0.1:8000/items/1" -H "accept: application/json"
```

## License

This project is licensed under the MIT License.