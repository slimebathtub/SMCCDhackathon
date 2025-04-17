# 🗂 Project Structure
This document describes the main folder and file structure of the SMCCDhackathon Django project.
Shuold be viewed after finishing all the prerequire (in README)

SMCCDhackathon/
├── campus_site/               # Main Django project configuration
│   ├── __init__.py              # Init for campus_site module
│   ├── asgi.py                  # ASGI config (for async deployment)
│   ├── settings.py              # Django settings (apps, middleware, DB etc.)
│   ├── urls.py                  # Root URL configuration
│   └── wsgi.py                  # WSGI config (for traditional deployment)
│
├── core/                      # Main app (resources, events, tutors…)
│   ├── admin.py                 # Django admin registration
│   ├── apps.py                  # App configuration
│   ├── models.py                # Database models go here
│   ├── views.py                 # View functions and logic
│   ├── urls.py                  # (Optional) App-specific routes
│   ├── templates/               # HTML templates (if used)
│   ├── static/                  # CSS, JS, images (if used)
│   └── migrations/              # Migration files for models
│       └── __init__.py
│
├── env/                       # Local virtual environment (excluded by .gitignore)
│
├── manage.py                  # Django project CLI entry point
├── requirements.txt           # Python packages required
├── .gitignore                 # Git ignored files config
├── README.md                  # Main project instruction file
└── PROJECT_STRUCTURE.md       # This file (project layout)

## 🧩 Proposed App Structure

| App Name       | Responsibility                          | Page/Feature              | Example Models                              |
|----------------|------------------------------------------|---------------------------|---------------------------------------------|
| `resources`    | Manage physical static items             | Page 1: Resources         | `Item`, `Category`, `Tag`, `ResourceEntity` |
| `rooms`        | Manage available room resources          | Page 2: Rooms             | `Room`, `Location`, `ResourceEntity`        |
| `calendar`     | Display and organize schedules/events    | Page 3: Now is Happening  | `Event`, `Tutor`, `CalendarEntity`          |
| `accounts`     | User login & permission (for centers)    | Backend only (login)      | Custom `User`, `CenterUser`, `Permission`   |
| `core` | Base models and reusable logic (abstract)| No UI                     | `ResourceEntity`, `CalendarEntity`          |

## 🏗 Models description
[View models describtion](https://docs.google.com/document/d/1Y6XKusWbk3OGrOPl2z1UXW5Vl6ZkiCO_fYxj55chb2Y/edit?usp=sharing)
core/
├── models/
│   ├── __init__.py         ← all the sub models
│   ├── base.py             ← ResourceEntity, CalendarEntity
│   ├── item.py             ← Item model
│   ├── room.py             ← Room model
│   ├── event.py            ← Event model
│   ├── tutor.py            ← Tutor model

---

## 🔑 Notes

- `core/` can later be split into more apps (e.g., `resources/`, `calendar/`) if project grows  
- Keep templates and static files inside each app or global folder depending on reuse  
- Make sure `env/` is excluded from commits using `.gitignore`  
- Use `requirements.txt` to record all external packages  

---
