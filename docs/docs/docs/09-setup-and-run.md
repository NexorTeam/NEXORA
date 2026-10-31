# راهنمای نصب و اجرا | Setup and Run Guide

## Proposed local setup
This section becomes final only after the team confirms Django/Python.

1. Install a supported Python version compatible with the chosen Django release.
2. Clone the repository.
3. Create and activate a virtual environment.
4. Install dependencies from `requirements.txt`.
5. Copy `.env.example` to `.env` if environment configuration is used; never commit real secrets.
6. Run database migrations.
7. Create a development superuser.
8. Start the local development server.
9. Open the local URL shown by Django.

## Example commands (Django proposal)
```bash
python -m venv .venv
# Windows PowerShell:
.venv\\Scripts\\Activate.ps1
# macOS/Linux:
source .venv/bin/activate

pip install -r requirements.txt
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
```

## Tests
```bash
python manage.py test
```

## Important
The current repository package is a planning/documentation baseline. These commands will work only after the Django project files and `requirements.txt` have been created and verified. Do not present the system as runnable until implementation is actually available.
