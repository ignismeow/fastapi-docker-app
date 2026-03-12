# FastAPI Docker App

A FastAPI application containerized with Docker and orchestrated with Docker Compose.

## Features

- FastAPI web framework for building APIs with Python 3.11
- Docker containerization for consistent deployment
- Docker Compose for easy local development and deployment
- CI/CD pipeline with GitHub Actions

## Prerequisites

- Docker
- Docker Compose
- Python 3.11 (for local development)

## Getting Started

### Local Development

1. Clone the repository:
   ```bash
   git clone https://github.com/ignismeow/fastapi-docker-app.git
   cd fastapi-docker-app
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the application:
   ```bash
   uvicorn main:app --host 0.0.0.0 --port 9000
   ```

### Using Docker

1. Build the Docker image:
   ```bash
   docker build -t fastapi-docker-app:latest .
   ```

2. Run the container:
   ```bash
   docker run -p 9000:9000 fastapi-docker-app:latest
   ```

### Using Docker Compose

1. Start the application:
   ```bash
   docker-compose up -d
   ```

2. Stop the application:
   ```bash
   docker-compose down
   ```

## Project Structure

```
fastapi-docker-app/
├── .github/
│   └── workflows/
│       └── ci.yml      # CI/CD pipeline configuration
├── Dockerfile          # Docker image definition
├── docker-compose.yml  # Docker Compose configuration
├── main.py             # FastAPI application
├── requirements.txt    # Python dependencies
└── README.md           # Project documentation
```

## CI/CD Pipeline

The project includes a CI/CD pipeline that:

- Runs tests on every push and pull request to main
- Builds and deploys the Docker image to production when changes are merged to main

## API Documentation

Once the application is running, visit:

- Swagger UI: http://localhost:9000/docs
- ReDoc: http://localhost:9000/redoc

## License

This project is licensed under the MIT License.