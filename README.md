# JobTrack — Job Application Tracker

A beginner-friendly portfolio project built with Python, Django, SQLite, Django REST Framework, and Bootstrap.

## Features
- User registration, login, logout
- Create, list, update, delete job applications
- Status tracking: Applied, Interview, Offer, Rejected
- Search by company or role
- Per-user data isolation
- Authenticated REST API
- Django admin and automated tests

## Local setup
Python 3.12 is recommended.

### Windows PowerShell
```powershell
py -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
pip install -r requirements.txt
python manage.py makemigrations applications
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
```

Open http://127.0.0.1:8000/ and register a user.

If PowerShell blocks activation, run `.venv\Scripts\python.exe` instead of activating the environment.

### macOS / Linux
```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
pip install -r requirements.txt
python manage.py makemigrations applications
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
```

## Useful URLs
- `/` — dashboard
- `/accounts/register/` — register
- `/accounts/login/` — login
- `/admin/` — admin site
- `/api/applications/` — REST API list/create
- `/api/applications/<id>/` — retrieve/update/delete one record

The API uses Django session or Basic Authentication and requires login. Use a test account only with Basic Authentication; do not send real credentials over plain HTTP.

## Tests
```bash
python manage.py test
```

## Production deployment checklist
1. Create a Git repository and push this project to GitHub.
2. Choose a Python-compatible hosting provider that supports Django and PostgreSQL.
3. Configure environment variables: `SECRET_KEY` (a long random secret), `DEBUG=False`, `ALLOWED_HOSTS=your-domain.example.com`, and `DATABASE_URL` (provider's PostgreSQL URL).
4. Set the build command to `pip install -r requirements.txt && python manage.py collectstatic --noinput && python manage.py migrate`.
5. Set the start command to `gunicorn config.wsgi:application`.
6. Ensure the host's persistent PostgreSQL database is connected; do not rely on SQLite on ephemeral hosting disks.
7. Run `python manage.py check --deploy`, test registration/login/CRUD/API on the live HTTPS site, and verify backups.
8. Configure HTTPS and any provider-specific CSRF trusted origins if needed.

For production, set a secure `SECRET_KEY`, `DEBUG=False`, a correct `ALLOWED_HOSTS`, and a persistent database. Never commit secrets or `.env` files to Git.
