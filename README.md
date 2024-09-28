# **FastAPI Task Manager**
This project implements a simple task manager API using FastAPI. It allows you to create, read, update, and delete tasks.

## Features
- **Create tasks**: Add new tasks with titles, optional descriptions, and completion status.
- **Read tasks**: Retrieve all tasks or a specific task by its unique identifier `UUID`.
- **Update tasks**: Modify existing tasks by providing updated details.
- **Delete tasks**: Remove unwanted tasks by their `UUIDs`.
- **Error handling**: Raises HTTP exceptions with appropriate status codes `404 Not Found` for missing resources.
## Installation
To run this API, you'll need Python 3.6 or later with the following libraries installed:

```
pip install fastapi uvicorn python-multipart
```

## Usage
Clone this repository or download the code.
Install the required dependencies (see Installation).

### Run the API server:
```
python main.py
```

### This starts the server on http://localhost:8080 (Windows). 
- Redirect to `http:/0.0.0.0:8000` (Mac)

Use tools like Postman, curl, or your preferred HTTP client to interact with the API endpoints:

### Create a task:
```
POST http://localhost:8080/tasks/
Content-Type: application/json

{
    "title": "Buy groceries",
    "description": "Milk, bread, eggs",
    "completed": False
}
```

### Read all tasks:
`GET http://localhost:8080/tasks/`
### Read a specific task:
`GET http://localhost:8080/tasks/{task_id}`
Replace `{task_id}` with the actual `UUID` of the task.

### Update a task:
```
PUT http://localhost:8080/tasks/{task_id}
Content-Type: application/json

{
    "title": "Updated title",
    "completed": True
}
```

### Delete a task:
`DELETE http://localhost:8080/tasks/{task_id}`
