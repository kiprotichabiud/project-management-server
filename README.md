# Project Management System Server

This Project Management System Server provides a robust backend for managing users, teams, and projects. Built with Flask and SQLAlchemy, it supports RESTful interactions and includes user authentication and validation features.

## Features
- User Management: Create, read, and validate users with email and password.
- Team Management: Create teams linked to users, and retrieve team details.
- Project Management: Create projects and associate users with them.
- Database Support: Utilizes SQLite for persistent storage.
- CORS Enabled: Supports cross-origin requests for seamless integration with frontend applications.
## Technologies Used
- Flask: A lightweight WSGI web application framework for Python.
- Flask-SQLAlchemy: An ORM for handling database interactions.
- Flask-CORS: A module for handling Cross-Origin Resource Sharing.
- Flask-Migrate: A database migration tool for SQLAlchemy.
- SQLAlchemy-Serializer: For serializing models to JSON.
## Installation
### Prerequisites
- Python 3.6 or higher
- pip (Python package installer)
### Steps to Install
1.  Clone the repository:

``git@github.com:kiprotichabiud/project-management-server.git``

``cd project-management-server``

2. Create a virtual environment:

``python -m venv venv``

3. Install dependencies:


``pip install -r requirements.txt``

4. Set up the database:


`` flask db init``

 ``flask db migrate``
 
 ``flask db upgrade``
 
5. Run the application:


``python app.py``
## API Endpoints
### Users
- GET /users: Retrieve a list of all users.
- POST /users: Create a new user.
- Body:
json

``{
  "username": "string",
  "email": "string",
  "name": "string",
  "password": "string"
}``
### Teams
- GET /teams: Retrieve a list of all teams.
- POST /teams: Create a new team.
- Body:
json

``{
  "name": "string",
  "description": "string",
  "user_id": "integer"
}``
### Projects
- GET /projects: Retrieve a list of all projects.
- POST /projects: Create a new project.
- Body:
json

``{
  "name": "string"
}``
### User Details
- GET /user/int:user_id: Retrieve detailed information about a user, including their teams and projects.
## Database Schema
- Users Table: Stores user details (id, username, email, name, password).
- Teams Table: Stores team details (id, title, description, user_id).
- Projects Table: Stores project details (id, name).
- User-Projects Association Table: Manages the many-to-many relationship between users and projects.
## Contribution
Contributions are welcome! To contribute:

- Fork the repository.
- Create a new branch: git checkout -b feature-branch.
- Make your changes.
- Commit your changes: git commit -m 'Add new feature'.
- Push to the branch: git push origin feature-branch.
- Create a Pull Request.

## License
This project is licensed under the MIT License.

## Acknowledgments
Thanks to the contributors and the open-source community for providing the tools and libraries that made this project possible!




