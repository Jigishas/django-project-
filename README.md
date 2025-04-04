# EARSS Project

A Django web application for managing media and user authentication.

## Project Structure

```
project/
├── app/                      # Main Django application
│   ├── migrations/           # Database migrations
│   ├── __init__.py
│   ├── models.py             # Database models
│   ├── tests.py              # Test cases
│   ├── urls.py               # Application URLs
│   └── views.py              # View functions
├── media/                    # Uploaded media files
│   └── pictures/             # User-uploaded pictures
├── project/                  # Project configuration
│   ├── __init__.py
│   ├── asgi.py               # ASGI config
│   ├── settings.py           # Django settings
│   ├── urls.py               # Project URLs
│   └── wsgi.py               # WSGI config
├── static/                   # Static files
│   ├── css/                  # CSS stylesheets
│   ├── js/                   # JavaScript files
│   └── media/                # Static media files
└── templates/                # HTML templates
    ├── index.html            # Main page
    ├── login.html            # Login page
    └── signin.html           # Signup page
```

## Installation

1. Clone the repository:
   ```bash
   git clone [repository_url]
   cd project
   ```

2. Create and activate virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Apply migrations:
   ```bash
   python manage.py migrate
   ```

5. Create superuser (optional):
   ```bash
   python manage.py createsuperuser
   ```

6. Run development server:
   ```bash
   python manage.py runserver
   ```

## Configuration

1. Set up environment variables in `project/settings.py`:
   - `SECRET_KEY`
   - `DEBUG` (set to `False` in production)
   - Database settings
   - Allowed hosts

2. For media files, ensure these settings in `settings.py`:
   ```python
   MEDIA_URL = '/media/'
   MEDIA_ROOT = os.path.join(BASE_DIR, 'media/')
   ```

## Features

- User authentication (login/signup)
- Media file management
- Static file serving
- Responsive templates

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
