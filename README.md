# FAQ_BharatFD_Project-
# Knowledge Base Manager

This is a Django-based web application designed to manage a structured knowledge base. The project allows users to create, categorize, and search articles, making information easily accessible. The system includes user authentication, role-based permissions, and API endpoints for integration.

## Features

- User authentication and role-based access control
- Categorization of knowledge base articles
- Full-text search functionality
- Markdown editor for rich text formatting
- REST API for retrieving articles and categories
- Docker support for seamless deployment

## Requirements

Ensure you have the following installed before running the project:

- Python 3.x
- Django 5.x
- PostgreSQL (or SQLite for development)
- Elasticsearch (for full-text search)
- Docker (optional for containerized deployment)

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/knowledge-base.git
cd knowledge-base
```

### 2. Set Up a Virtual Environment

```bash
python -m venv venv
```

Activate the virtual environment:

Windows:

```bash
venv\Scripts\activate
```

Mac/Linux:

```bash
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure the Database

Modify `settings.py` to configure your PostgreSQL database. Then, run migrations:

```bash
python manage.py migrate
```

### 5. Create a Superuser

```bash
python manage.py createsuperuser
```

Follow the prompts to set up your admin credentials.

### 6. Start the Development Server

```bash
python manage.py runserver
```

Access the application at [http://127.0.0.1:8000/](http://127.0.0.1:8000/).

## API Usage

### Endpoints

- `GET /api/articles/` - Retrieve all articles
- `GET /api/articles/?category=<category_name>` - Retrieve articles by category
- `GET /api/articles/?search=<query>` - Perform a full-text search

### Example API Calls

Retrieve all articles:
```bash
curl http://127.0.0.1:8000/api/articles/
```

Search articles:
```bash
curl http://127.0.0.1:8000/api/articles/?search=django
```

## Deployment with Docker

Build and run the application with Docker:

```bash
docker-compose up --build
```

## Contributing

1. Fork the repository.
2. Create a feature branch (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -m "Add feature"`).
4. Push the branch (`git push origin feature-branch`).
5. Open a pull request.

## License

This project is licensed under the MIT License. See the LICENSE file for details.

## Acknowledgments

- Django for the web framework.
- PostgreSQL for database management.
- Elasticsearch for full-text search capabilities.
- Docker for containerized deployment.

