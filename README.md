Here is your **complete professional README** — copy-paste fully into `README.md`:

---

````markdown
# Item Management REST API

## Live Application
https://item-api-1-zw6f.onrender.com

## GitHub Repository
https://github.com/Chandu639/item-api

---

## Project Overview

This project is a simple Spring Boot RESTful API that manages a collection of items in an e-commerce style system.  
The application uses in-memory storage (ArrayList) as required and provides endpoints to add and retrieve items.

The application is containerized using Docker and deployed on Render.

---

## Tech Stack

- Java 21
- Spring Boot 3.2.5
- Spring Web
- Jakarta Validation
- Maven
- Docker
- Render (Cloud Hosting)

---

## Features

- Add a new item
- Retrieve an item by ID
- Input validation for required fields
- In-memory data storage (no database)
- Dockerized deployment
- Public cloud hosting

---

## API Endpoints

### 1️⃣ Add Item

**POST** `/api/items`

#### Request Body (JSON)

```json
{
  "name": "Laptop",
  "description": "Dell Inspiron",
  "price": 55000
}
````

#### Success Response

```json
{
  "id": 1,
  "name": "Laptop",
  "description": "Dell Inspiron",
  "price": 55000
}
```

---

### 2️⃣ Get Item By ID

**GET** `/api/items/{id}`

#### Example

```
GET /api/items/1
```

#### Response

```json
{
  "id": 1,
  "name": "Laptop",
  "description": "Dell Inspiron",
  "price": 55000
}
```

---

## Input Validation

The following validations are implemented using Jakarta Validation:

* `name` → Required (Not Blank)
* `description` → Required (Not Blank)
* `price` → Required (Not Null)

If invalid data is submitted, the API returns appropriate validation errors.

---

## Project Structure

```
item-api/
 ├── Dockerfile
 ├── pom.xml
 ├── README.md
 └── src/
     └── main/java/com/item/
         ├── ItemApiApplication.java
         ├── controller/ItemController.java
         ├── service/ItemService.java
         └── model/Item.java
```

---

## Running Locally

### 1. Clone Repository

```
git clone https://github.com/Chandu639/item-api.git
```

### 2. Navigate to Project

```
cd item-api
```

### 3. Build Project

```
mvn clean package
```

### 4. Run Application

```
java -jar target/itemapi-0.0.1-SNAPSHOT.jar
```

Application runs on:

```
http://localhost:8080
```

---

## Deployment Details

The application is:

* Containerized using Docker
* Built inside Docker using Maven
* Deployed on Render Cloud
* Configured to use dynamic PORT binding

---

## Notes

* Data is stored in memory (ArrayList)
* No database integration as per requirement
* Designed to be simple, clean, and easily extendable
* Can be enhanced with full CRUD operations, database integration, and exception handling

---

## Author

T Venkata Chandra Krishna

```
