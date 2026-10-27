# Django Phone Store

A clean and responsive mobile phone catalog application built using the Django web framework. The project dynamically handles phone inventories, details, and media assets using Django's ORM, models, and template architecture.

## 📱 Features

- **Dynamic Product Catalog:** Automatically loads phone listings from the database with attributes for Brand, Model, Price, and Images.
- **Modern Responsive UI:** Features a sleek product grid built with Flexbox/CSS Grid, complete with hover animations, rounded card styles, and drop-shadow styling.
- **Media Asset Integration:** Leverages Django's media storage pipeline to host and render authentic product photos safely.
- **Robust Admin Dashboard:** Full CRUD operations enabled out-of-the-box via Django Admin to seamlessly manage active storefront entries.

## 🛠️ Tech Stack

- **Backend:** Python 3.14+, Django 6.0+
- **Database:** SQLite (default/development)
- **Frontend:** HTML5, CSS3 (Flexbox/Grid), Django Template Language (DTL)

## 📁 File Structure Overview

```text
phone_store/
 │
 ├── app_catalog/            # Core application directory
 │    ├── migrations/        # Database versioning files
 │    ├── static/catalog/    # Frontend CSS stylesheets (styles.css)
 │    ├── templates/         # HTML template architecture (base, list, detail)
 │    ├── models.py          # Database schema (Phone configurations)
 │    ├── views.py           # Controller / Routing request logic
 │    └── urls.py            # Local application URL configurations
 │
 ├── media/phone_images/     # Uploaded product image assets
 ├── phone_store/            # Project configuration files (settings.py, urls.py)
 └── manage.py               # Django command-line execution utility
```

## 🚀 Installation & Local Setup

Follow these steps to get the development environment running locally.

### 1. Clone the Repository
```bash
git clone https://github.com
cd phone_store
```

### 2. Set Up a Virtual Environment (Optional but Recommended)
```bash
python -m venv venv
# Activate on Windows:
venv\Scripts\activate
# Activate on macOS/Linux:
source venv/bin/activate
```

### 3. Install Dependencies
Make sure Django is installed. If you have a requirements file, run:
```bash
pip install -r requirements.txt
```

### 4. Apply Database Migrations
Generate and initialize your local SQLite database structures:
```bash
python manage.py makemigrations
python manage.py migrate
```

### 5. Create a Superuser (For Admin Access)
Create an account to log into the backend and add phones:
```bash
python manage.py createsuperuser
```

### 6. Boot Up the Development Server
```bash
python manage.py runserver
```
Open your browser and navigate to `http://127.0.0` to view the catalog or `http://127.0.0admin/` to upload products.

## 🔒 Security Best Practices
Before pushing this code to a production server, make sure to:
- Change `DEBUG = True` to `False` inside `settings.py`.
- Move your `SECRET_KEY` into an isolated environment variable using a `.env` file.
- Keep `db.sqlite3` and the local `media/` directory within your `.gitignore`.
