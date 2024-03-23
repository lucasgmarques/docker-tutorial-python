# Flask PostgreSQL Example

This is a simple Flask application that demonstrates how to connect to a PostgreSQL database to perform basic CRUD operations. The application provides endpoints to fetch widgets from the database and initialize the database schema.

## Setup

### Prerequisites

-   Python 3.x
-   PostgreSQL

### Installation

1.  Clone the repository:
    
    
    `git clone https://github.com/your_username/flask-postgresql-example.git` 
    
2.  Navigate to the project directory:
    
    
    `cd flask-postgresql-example` 
    
3.  Install dependencies using pip:
    
    
    `pip install -r requirements.txt` 
    

## Configuration

This application uses environment variables for configuration. You need to set the following environment variables:

-   `POSTGRES_PASSWORD_FILE`: Path to the file containing the PostgreSQL password.
-   `POSTGRES_PASSWORD`: PostgreSQL password (fallback if `POSTGRES_PASSWORD_FILE` is not set).

## Running the Application

Run the following command to start the Flask application:

`python app.py` 

By default, the application will run on `http://localhost:5000`.

## Endpoints

### 1. `/`

-   **Method:** GET
-   **Description:** Returns a simple greeting message.
-   **Example Response:**
    
    `Hello, Docker!!!` 
    

### 2. `/widgets`

-   **Method:** GET
-   **Description:** Retrieves all widgets from the PostgreSQL database.
-   **Example Response:**
    
    
    `[
      {"name": "Widget 1", "description": "Description 1"},
      {"name": "Widget 2", "description": "Description 2"},
      ...
    ]` 
    

### 3. `/initdb`

-   **Method:** GET
-   **Description:** Initializes the PostgreSQL database schema.
-   **Example Response:**
    
    
    `init database` 
    

## Database Schema

The application uses a single table named `widgets` with the following schema:

-   `name`: VARCHAR(255)
-   `description`: VARCHAR(255)

## Dependencies

-   Flask: Web framework for building the application.
-   psycopg2: PostgreSQL adapter for Python.
