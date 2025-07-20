# TukeTube - Django Video Website

A Django-powered video sharing platform with user authentication, video upload, and interactive features.

## Features

- 🎥 Video upload and streaming
- 👤 User authentication (login/signup)
- 👍 Like/Dislike functionality with toggle
- 💬 Comment system
- 📱 Responsive design with Bootstrap
- 🔍 Video search functionality
- 📄 Pagination

## Tech Stack

- **Backend**: Django 4.2
- **Frontend**: Bootstrap 5, HTML5, CSS3, JavaScript
- **Database**: SQLite (development)
- **Icons**: Font Awesome
- **Video Player**: Custom HTML5 video player

## Installation & Setup

### Prerequisites
- Python 3.10+
- pip (Python package manager)

### 1. Clone the Repository
```bash
git clone <repository-url>
cd Django-Tube-Video-Website-Powered-By-Django
```

### 2. Create Virtual Environment
```bash
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Environment Configuration
```bash
cp .env.example .env
# Edit .env file with your configuration
```

### 5. Database Setup
```bash
cd src
python manage.py makemigrations
python manage.py migrate
```

### 6. Create Superuser (Optional)
```bash
python manage.py createsuperuser
```

### 7. Run Development Server
```bash
python manage.py runserver
```

Visit `http://127.0.0.1:8000` to view the application.

## Project Structure

```
Django-Tube-Video-Website-Powered-By-Django/
├── .gitignore                    # Git ignore file
├── .env.example                  # Environment variables template
├── requirements.txt              # Python dependencies
├── venv/                        # Virtual environment (ignored)
└── src/                         # Django project source
    ├── manage.py                # Django management script
    ├── db.sqlite3              # SQLite database
    ├── media/                  # User uploaded media
    │   ├── images/            # User profile pictures & thumbnails
    │   └── videos/            # Uploaded videos
    ├── static/                # Static files
    ├── templates/             # Global templates
    ├── config/                # Django project configuration
    │   ├── settings.py        # Main settings
    │   ├── urls.py           # Main URL configuration
    │   └── wsgi.py           # WSGI configuration
    ├── accounts/              # User authentication app
    │   ├── models.py         # User profile models
    │   ├── views.py          # Authentication views
    │   ├── urls.py           # Authentication URLs
    │   └── templates/        # Auth templates (login/signup)
    └── videos/                # Main video app
        ├── models.py          # Video, Comment, Rating models
        ├── views.py           # Video-related views
        ├── urls.py            # Video URLs
        ├── admin.py           # Admin configuration
        ├── templatetags/      # Custom template tags
        ├── templates/         # Video templates
        └── static/            # Video app static files
```

## Usage

### For Users
1. **Sign Up**: Create a new account
2. **Login**: Access your account
3. **Upload Videos**: Share your content
4. **Browse Videos**: Discover content from other users
5. **Interact**: Like, dislike, and comment on videos

### For Developers
- Models are in respective `models.py` files
- Views follow Django best practices
- Templates use Bootstrap for responsive design
- Static files are organized by app
- Custom template tags in `videos/templatetags/`

## Key Features Implementation

### Toggle Like/Dislike System
- Users can like or dislike videos
- Clicking the same button again removes the rating
- Switching between like/dislike updates counts accordingly
- Visual feedback shows current user rating state

### Video Upload
- Support for various video formats
- Automatic thumbnail generation
- File validation and security

### Responsive Design
- Mobile-first Bootstrap implementation
- Professional UI across all pages
- Consistent design language

## Development

### Running Tests
```bash
python manage.py test
```

### Creating Migrations
```bash
python manage.py makemigrations
python manage.py migrate
```

### Collecting Static Files (Production)
```bash
python manage.py collectstatic
```

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Run tests
5. Submit a pull request

## License

This project is open source and available under the [MIT License](LICENSE).

## Support

For support, please open an issue on the GitHub repository.
