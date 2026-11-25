# Job Application Tracker

A Django-based web application to track and manage job applications.

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![Django](https://img.shields.io/badge/Django-092E20?logo=django&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1)
![Bootstrap](https://img.shields.io/badge/Bootstrap-7952B3?logo=bootstrap&logoColor=white)

## Features

- Add, update and delete job applications
- Search applications
- Application status management
- Database integration

## Tech Stack

- **Backend:** Python, Django
- **Database:** SQL (SQLite)
- **Frontend:** HTML, Bootstrap

## Getting Started

1. Clone the repository

```bash
git clone https://github.com/Yaswanthnaikk/Job-Application-Tracker.git
cd Job-Application-Tracker
```

2. Create and activate a virtual environment

```bash
python -m venv venv
venv\Scripts\activate        # Windows
source venv/bin/activate      # macOS / Linux
```

3. Install dependencies

```bash
pip install -r requirements.txt
```

4. Apply migrations and create an admin user

```bash
python manage.py migrate
python manage.py createsuperuser
```

5. Run the server

```bash
python manage.py runserver
```

Open http://127.0.0.1:8000/ in your browser.

<!-- Add screenshots here: create a "screenshots" folder in the repo, upload images, then use ![Home page](screenshots/home.png) -->

## What I Learned

- Implementing search and status management
- Django views, templates and URL routing
- Database integration with SQL

## Author

**Yaswanth Naik Desavath**
[GitHub](https://github.com/Yaswanthnaikk) | [LinkedIn](https://linkedin.com/in/yaswanth-naik) | dyaswanthnaiknaik@gmail.com
