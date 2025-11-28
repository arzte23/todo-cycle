# Todo Cycle

Todo Cycle is a Django/DRF application for managing tasks with recurrence rules and notifications.  
It is designed as a practical tool for personal use, family, and friends, with a focus on mobile-first experience.

## 🚀 Quick Start

### Installation and Run
```bash
# Clone the repository
git clone https://github.com/arzte23/todo-cycle.git
cd todo-cycle

# Create and activate virtual environment
python3 -m venv .venv
source .venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Create .env file
echo "SECRET_KEY=change-me-please" > .env
echo "DEBUG=true" >> .env
echo "ALLOWED_HOSTS=localhost,127.0.0.1" >> .env

# Apply migrations
python manage.py makemigrations
python manage.py migrate

# Create superuser
python manage.py createsuperuser

# Run server
python manage.py runserver
```

## Authentication
- Uses JWT via djangorestframework-simplejwt.
- Endpoints:
  - POST /api/auth/token/ — obtain token (login).
  - POST /api/auth/token/refresh/ — refresh token.

## Current Status
- ✅ Django project initialized.
- ✅ accounts app created with custom User model.
- ✅ DRF and JWT configured.
- ✅ .env integrated via environs.

## 📌 Next Steps
- Add tasks app with models for tasks, recurrence, and notifications.
- Implement CRUD API for tasks.
- Add frontend (Bootstrap + HTMX).
- Deploy on free hosting (Render/Fly.io).
