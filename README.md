# Fruit.ai Backend

This repository contains the backend for **FruitAI**, a health management application. Developed with Flask, the backend provides essential CRUD functionality for managing fruit-related FAQs. It handles server-side logic, database operations using **MongoDB**, and interacts with the frontend to power the application’s features.

## Features

- **CRUD Operations**: Create, Read, Update, Delete FAQs.
- **Error Handling**: Comprehensive error handling for both client-side and server-side issues.
- **Database Integration**: Uses MongoDB for storage.
- **Modular Design**: Adheres to a clean architecture with distinct files for models and routes.

## Technologies Used

- **Flask**: Micro-framework for building web applications.
- **PyMongo**: Python driver for interacting with MongoDB.
- **MongoDB**: NoSQL database for managing FAQs.
- **Postman**: Tool for API testing and development.
- **Python 3.8+**

## API Endpoints

| Method | Endpoint       | Description                  |
|--------|----------------|------------------------------|
| GET    | `/faqs`        | Fetch all FAQs               |
| GET    | `/faqs/<id>`   | Fetch a single FAQ by ID     |
| POST   | `/faqs`        | Create a new FAQ             |
| PUT    | `/faqs/<id>`   | Update an existing FAQ       |
| DELETE | `/faqs/<id>`   | Delete a FAQ by ID           |

## Error Handling

- **404 Not Found**: Returned when the requested resource does not exist.
- **500 Internal Server Error**: Returned for any unhandled server-side exceptions.
- **400 Bad Request**: Returned when invalid data is provided.

## Setup Instructions

### Prerequisites

- Python 3.8+
- pip (Python package manager)
- MongoDB (Ensure MongoDB is installed and running on your machine or use a cloud instance like MongoDB Atlas)

### Installation

1. **Clone the Repository**
    ```bash
    git clone https://github.com/Ishayadav5299/FruitAI-Backend-Project.git
    cd FruitAI-Backend-Project
    ```

2. **Create a Virtual Environment**
    ```bash
    python3 -m venv venv
    source venv/bin/activate   # For Linux/macOS
    # OR
    venv\Scripts\activate      # For Windows
    ```

3. **Install Dependencies**
    ```bash
    pip install -r requirements.txt
    ```

4. **Configure MongoDB**
    - Ensure MongoDB is running locally, or configure it with a remote MongoDB URL by adding the MongoDB URI to an `.env` file:
    ```bash
    MONGO_URI=mongodb://localhost:27017/fruitdb
    ```

5. **Run the Application**
    ```bash
    python app.py
    ```

   The application will be running on `http://localhost:5000`.

## Project Structure

```bash
fruit-ai-backend/
├── migrations/          # Database migrations folder
│   └── ...              # Migration files (e.g., versions of schema changes)
├── .gitignore           # Ignoring unnecessary files (e.g., virtual env, compiled files)
├── Procfile             # File for deploying on Heroku or similar platforms
├── app.py               # Main Flask application
├── requirements.txt     # Python dependencies
├── README.md            # Project documentation
└── venv/                # Virtual environment (not included in Git)

```

## Design Decisions

- **Flask Framework**: Selected for its simplicity and flexibility, which makes it well-suited for rapid development.
- **PyMongo and MongoDB**: MongoDB offers scalability, flexibility, and ease of use for managing a document-based data structure.
- **Postman**: Used for API testing to verify that all endpoints operate correctly and meet the specified requirements.

## MongoDB Configuration

To change the MongoDB connection, you can set a custom `MONGO_URI` in the `.env` file. The default URI connects to a local MongoDB instance running on `localhost:27017`:

```
MONGO_URI=mongodb://localhost:27017/fruitdb
```

Alternatively, if using MongoDB Atlas (cloud-hosted), you can set the connection string accordingly.

## License

This project is licensed under the MIT License.
