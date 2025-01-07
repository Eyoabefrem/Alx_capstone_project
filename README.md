# AfroConnect API

The **AfroConnect API** is a backend service designed for a social media platform tailored to African communities and cultures. Built with Django and Django REST Framework (DRF), this API provides a robust set of features for user management, post creation, and social interactions.

## Features

### Core Functionalities
1. **User Management**
   - User registration and authentication.
   - View and update user profiles with optional fields like bio and profile picture.

2. **Post Management**
   - Create, read, update, and delete posts.
   - Posts can include text and optional media attachments.

3. **Follow System**
   - Follow and unfollow other users.
   - Retrieve lists of followers and following.

4. **Feed Management**
   - Personalized feed displaying posts from followed users in reverse chronological order.

### Technical Highlights
- **Django ORM** for database interactions.
- **JWT Authentication** for secure API access.
- Pagination and sorting for large datasets.
- RESTful API design with appropriate HTTP methods and status codes.

---

## API Endpoints

### User Endpoints
| Method | Endpoint             | Description                        |
|--------|----------------------|------------------------------------|
| POST   | `/api/register/`     | Register a new user.              |
| POST   | `/api/login/`        | Log in an existing user.          |
| POST   | `/api/logout/`       | Log out the current user.         |
| GET    | `/api/users/<user_id>/` | View user profile.                |
| PUT    | `/api/users/<user_id>/` | Update user profile.              |

### Post Endpoints
| Method | Endpoint           | Description                        |
|--------|--------------------|------------------------------------|
| POST   | `/api/posts/`      | Create a new post.                |
| GET    | `/api/posts/`      | Retrieve a list of posts.         |
| GET    | `/api/posts/<post_id>/` | Retrieve a specific post.        |
| PUT    | `/api/posts/<post_id>/` | Update a specific post.          |
| DELETE | `/api/posts/<post_id>/` | Delete a specific post.          |

### Follow System Endpoints
| Method | Endpoint          | Description                        |
|--------|-------------------|------------------------------------|
| POST   | `/api/follow/`    | Follow a user.                    |
| POST   | `/api/unfollow/`  | Unfollow a user.                  |
| GET    | `/api/followers/` | Get the list of followers.        |
| GET    | `/api/following/` | Get the list of followed users.   |

### Feed Endpoint
| Method | Endpoint   | Description                              |
|--------|------------|------------------------------------------|
| GET    | `/api/feed/` | Retrieve the personalized user feed.    |

---

## Installation

### Prerequisites
- Python 3.8+
- Django 4.0+
- PostgreSQL (optional but recommended for production)

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/username/afroconnect-api.git
   cd afroconnect-api
   ```
2. Create a virtual environment and activate it:
   ```bash
   python -m venv env
   source env/bin/activate   # For Windows: env\Scripts\activate
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Apply migrations:
   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```
5. Run the development server:
   ```bash
   python manage.py runserver
   ```

---

## Deployment

### Heroku Deployment
1. Install Heroku CLI and log in:
   ```bash
   heroku login
   ```
2. Create a Heroku app:
   ```bash
   heroku create afroconnect-api
   ```
3. Push the code to Heroku:
   ```bash
   git push heroku main
   ```
4. Configure environment variables (e.g., `DATABASE_URL`, `SECRET_KEY`) in the Heroku dashboard.

### PythonAnywhere Deployment
Follow [PythonAnywhere's guide](https://help.pythonanywhere.com/pages/DeployingDjango/) to deploy your application.

---

## Testing

### Run Tests
Execute the test suite to ensure everything works correctly:
```bash
python manage.py test
```

### Postman Collection
Use the provided Postman collection (`postman_collection.json`) for testing API endpoints. Import the file into Postman to start.

---

## Future Enhancements
- Add likes and comments to posts.
- Implement notifications for follows, likes, and comments.
- Advanced search functionality for posts and users.

---

## Contributing
1. Fork the repository.
2. Create a new branch for your feature:
   ```bash
   git checkout -b feature-name
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add a brief message describing your changes"
   ```
4. Push to your fork and submit a pull request.

---

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.

---

## Contact
For any inquiries or feedback, please reach out to:
- Email: support@afroconnect.com
- GitHub: [AfroConnect API](https://github.com/username/afroconnect-api)

