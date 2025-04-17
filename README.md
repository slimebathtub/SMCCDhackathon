# SMCCDhackathon

## 🧰 Project Requirements
- Python 3.10 or above
- Virtual environment recommended (venv)
- Django 5.1.7
- Git + GitHub

## 📦 Installation & Setup Guide (for team members)
### ✅ Step 1: Clone the Repository
### ✅ Step 2: (recommend) Create and Activate Virtual Environment
    ```bash
        python -m venv env
        source env/bin/activate  # Mac/Linux
        # Or on Windows: env\Scripts\activate
    ```
    Don't upload your venv (env) to github! (If you have do)
    Basically the way don't upload is already in .gitignore, so don't delete that file
### ✅ Step 3: Install Required Packages
    ```bash
    pip install -r requirements.txt
    ```
### ✅ Step 4: Testing if Djanga have successfully set up
    1. Apply Database Migrations

    ```bash
    python manage.py migrate
    ```
    2. Start Development Server

    ```bash
    python manage.py runserver
    ```

    3. Then open your browser to: http://127.0.0.1:8000/ and test

## 📂 Project Structure
    [View Project Structure](./PROJECT_STRUCTURE.md)


## 🧪 Developer Tips for GitHub
    - After pulling changes from GitHub:
```bash
git pull
source env/bin/activate
pip install -r requirements.txt
```


## 🧪 Developer Tips for Django
    - After modifying models:
  ```bash
  python manage.py makemigrations
  python manage.py migrate
  ```

    - To create an admin user: ( If you are not sure what is admin user, you can don't create first and ask @liyixin)
  ```bash
  python manage.py createsuperuser
  ```