# PSU_Sphere-Docker

This repository contains the Docker configuration for the PSUSphere Django project.
It allows anyone to run the application with a single command, either by building locally or pulling the prebuilt image from Docker Hub.

### How to Install?

📦 Prerequisites
- Install Docker Desktop
- Ensure Docker is running on your machine
- Verify installation:

docker --version
docker-compose --version

🚀 Running the Application
Option 1: Local Build (Developer Mode)
- Build and run the image directly from the Dockerfile: docker-compose up -d

Check logs:
docker-compose logs -f web

Access the app at: http://localhost:8000

Option 2: Client Mode (Pull from Docker Hub)
- Run the prebuilt image from Docker Hub (kimmy0621/django-app:latest):docker-compose -f for_client/docker-compose.yml up -d

Access the app at: http://localhost:8000

🔑 Initial Setup (First Time Only)
- Create a superuser for Django admin: docker-compose exec web python manage.py createsuperuser

Collect static files:
docker-compose exec web python manage.py collectstatic --noinput

📂 Repository Contents
- Dockerfile – build instructions for the image
- docker-compose.yml – local build configuration
- requirements.txt – Python dependencies
- .dockerignore – ignored files during build
- for_client/docker-compose.yml – client configuration (pull from Docker Hub)
- README.md – installation and usage instructions

✅ This README is tailored for your Docker repo submission — clean, minimal, and focused only on containerization.

## Author:
### Kim Andrei D. Padrones - BSCS3B2