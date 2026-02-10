Item Management REST API

This project is a simple Java backend application built using Spring Boot.
It exposes REST APIs to manage a collection of items and uses in-memory storage for simplicity.

The application was created as part of a sample task to demonstrate basic backend development concepts such as RESTful APIs, input validation, and clean code structure.
Tech Stack Used :

 1.   Java 17
 2.  Spring Boot
 3.  Maven
 4. Spring Web
 5. Bean Validation

What This Application Does:

  1.  Allows adding new items through a REST API
  2. Allows fetching a single item using its ID
  3. Performs basic validation on input data
  4. Stores data in memory using an ArrayList (no database involved)

Project Structure (High Level):

  1.  controller – Contains REST endpoints
  2.  service – Handles business logic and in-memory storage
  3.  model – Represents the Item data model

Running the Application Locally
  1.  Prerequisites
  2.  Java 17 installed
  3.  Maven installed

Steps to Run:
    
  1.  Clone the repository
  2.  Navigate to the project folder
  3.  Run the application using the command below:
  4.  mvn spring-boot:run


The application will start on:

http://localhost:8080

API Details
Add a New Item

Endpoint: POST /api/items


Request Body:
    {
    "name": "MacBook Pro",
    "description": "Apple laptop"
    }


Description : Creates a new item and assigns it a unique ID automatically.

Get Item by ID:

Endpoint : GET /api/items/{id}


Example

GET /api/items/1


Description
    Fetches a single item based on the provided ID.
    If the item does not exist, a 404 response is returned.

Validation
    The name field is mandatory while creating an item
    If required fields are missing, the API returns a 400 Bad Request response

Important Notes

  1.  This application uses in-memory storage, so all data will be lost when the server restarts
  2.  The project is intentionally kept simple to focus on core backend concepts
  3.  No database or authentication is implemented as it is not required for this task

Author
Divyansh Uniyal