# Django Tweet Application

A simple Twitter-like application built with Django where users can create, edit, and delete tweets with photo uploads.

## Features

- User registration and authentication
- Create, edit, and delete tweets
- Upload photos with tweets
- User-specific tweet management
- Responsive UI with Bootstrap

## Requirements

- Python 3.13+
- Django 6.0.3
- Pillow (for image handling)

## Installation

1. Clone the repository
```bash
cd djangoNew
```

2. Create virtual environment
```bash
python -m venv venv
venv\Scripts\activate
```

3. Install dependencies
```bash
pip install django pillow
```

4. Run migrations
```bash
cd chaiCenter
python manage.py migrate
```

5. Create superuser (optional)
```bash
python manage.py createsuperuser
```

6. Run the server
```bash
python manage.py runserver
```

7. Visit `http://127.0.0.1:8000/`

## Usage

- **Register**: Create a new account at `/tweet/register/`
- **Login**: Login at `/accounts/login/`
- **Create Tweet**: Click "Tweet Home" and create new tweets
- **Edit/Delete**: Manage your own tweets from the tweet list

## Project Structure

```
chaiCenter/
├── tweet/              # Main app
│   ├── models.py       # Tweet model
│   ├── views.py        # Views for CRUD operations
│   ├── forms.py        # Tweet and registration forms
│   └── urls.py         # App URLs
├── templates/
│   ├── Registration/   # Auth templates
│   └── layout.html     # Base template
└── manage.py
```

## Models

**Tweet**
- user (ForeignKey to User)
- text (TextField, max 240 chars)
- photo (ImageField, optional)
- created_at (DateTime)
- updated_at (DateTime)

## License

MIT
