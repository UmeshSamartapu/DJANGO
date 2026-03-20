Here’s a **clear, practical Django setup guide** (from zero → advanced), followed by a **complete command table** (beginner → intermediate → advanced).

---

# 🚀 1. Django Setup (Step-by-Step)

## ✅ Step 1: Install Python

* Install from: Python
* Check:

```bash
python --version
```

---

## ✅ Step 2: Create Virtual Environment

```bash
python -m venv env
```

Activate:

```bash
# Windows
env\Scripts\activate

# Linux/Mac
source env/bin/activate
```

---

## ✅ Step 3: Install Django

```bash
pip install django
```

Check version:

```bash
django-admin --version
```

---

## ✅ Step 4: Create Project

```bash
django-admin startproject myproject
cd myproject
```

Run server:

```bash
python manage.py runserver
```

👉 Open: [http://127.0.0.1:8000/](http://127.0.0.1:8000/)

---

## ✅ Step 5: Create App

```bash
python manage.py startapp myapp
```

Add in `settings.py`:

```python
INSTALLED_APPS = [
    'myapp',
]
```

---

## ✅ Step 6: Basic Flow (Important 🔥)

```
User → URL → View → Model → Database → Response → Template
```

---

## ✅ Step 7: Migrations (Database Setup)

```bash
python manage.py makemigrations
python manage.py migrate
```

---

## ✅ Step 8: Create Superuser (Admin)

```bash
python manage.py createsuperuser
```

---

## ✅ Step 9: Run Project

```bash
python manage.py runserver
```

---

# ⚡ Django Learning Levels

---

# 🟢 Beginner Level (Core Commands)

| Command                                 | Purpose               |
| --------------------------------------- | --------------------- |
| `django-admin startproject projectname` | Create new project    |
| `python manage.py runserver`            | Start server          |
| `python manage.py startapp appname`     | Create app            |
| `python manage.py makemigrations`       | Create DB migrations  |
| `python manage.py migrate`              | Apply migrations      |
| `python manage.py createsuperuser`      | Create admin user     |
| `python manage.py shell`                | Open Python shell     |
| `python manage.py showmigrations`       | Show migration status |

---

# 🟡 Intermediate Level (Development + Debugging)

| Command                                | Purpose                 |
| -------------------------------------- | ----------------------- |
| `python manage.py collectstatic`       | Collect static files    |
| `python manage.py flush`               | Delete all data from DB |
| `python manage.py dbshell`             | Open database shell     |
| `python manage.py sqlmigrate app 0001` | View SQL for migration  |
| `python manage.py inspectdb`           | Generate models from DB |
| `python manage.py dumpdata`            | Export DB data          |
| `python manage.py loaddata`            | Import DB data          |
| `python manage.py check`               | Check project issues    |
| `python manage.py test`                | Run tests               |
| `python manage.py diffsettings`        | Compare settings        |

---

# 🔴 Advanced Level (Production + Optimization)

| Command                                    | Purpose                                |
| ------------------------------------------ | -------------------------------------- |
| `python manage.py collectstatic --noinput` | Collect static for production          |
| `python manage.py clearsessions`           | Delete expired sessions                |
| `python manage.py shell_plus`              | Advanced shell (via django-extensions) |
| `python manage.py runserver 0.0.0.0:8000`  | Run on network                         |
| `python manage.py migrate --fake`          | Fake migrations                        |
| `python manage.py migrate app zero`        | Reset app migrations                   |
| `python manage.py squashmigrations app`    | Optimize migrations                    |
| `python manage.py changepassword user`     | Change user password                   |
| `python manage.py compilemessages`         | Compile translations                   |
| `python manage.py sendtestemail`           | Test email config                      |

---

# 🧠 Pro Tips (Very Important)

### ✅ Use Virtual Environment ALWAYS

Avoid dependency conflicts.

### ✅ Project Structure (Simple)

```
myproject/
 ├── manage.py
 ├── myproject/
 ├── myapp/
 ├── db.sqlite3
```

### ✅ Most Used Commands Daily

```bash
python manage.py runserver
python manage.py makemigrations
python manage.py migrate
```

---

# 🔥 Bonus: Full Dev Workflow

```bash
# Setup
python -m venv env
env\Scripts\activate
pip install django

# Project
django-admin startproject myproject
cd myproject

# App
python manage.py startapp myapp

# DB
python manage.py makemigrations
python manage.py migrate

# Run
python manage.py runserver
```

---


"# DJANGO" 
