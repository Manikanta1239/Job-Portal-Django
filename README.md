# Django Job Portal

A full-featured job portal application built with Django that connects job seekers and employers.

## 📚 Detailed Overview

### For Job Seekers
- Create your professional profile
- Upload resume (Supported formats: PDF, DOC, DOCX)
- Search jobs by:
  - Keywords
  - Location
  - Job Type (Full-time, Part-time, Remote)
  - Experience Level
- Track application status (Applied, Under Review, Accepted, Rejected)
- Receive email notifications for application updates

### For Employers
- Company profile management
- Post unlimited job listings with details:
  - Job description
  - Required skills
  - Salary range
  - Location options
- Review candidate applications
- Download candidate resumes
- Track applicant statistics

## ✨ Features

- User authentication (Job Seeker & Employer)
- Job posting and management
- Job applications tracking
- Job search and filtering
- User dashboard
- Responsive design
- Email notifications

## 🔍 Detailed Setup Guide

### Prerequisites Explained
1. **Python 3.8+**
   - Download from python.org
   - Verify installation: `python --version`

2. **pip (Python Package Manager)**
   - Should be included with Python
   - Verify installation: `pip --version`

3. **Virtual Environment**
   - Keeps project dependencies isolated
   - Prevents conflicts between projects

### Step-by-Step Installation

1. **Project Setup**
```bash
# Clone repository
git clone https://github.com/Manikanta1239/Job-Portal-Django.git
cd Job-Portal-Django

# Create virtual environment
python -m venv venv

# Activate virtual environment
# Windows:
venv\Scripts\activate
# Linux/Mac:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt
```

2. **Database Configuration**
```python
# settings.py configuration options:

# For SQLite (Default)
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.sqlite3',
        'NAME': BASE_DIR / 'db.sqlite3',
    }
}

# For PostgreSQL (Recommended for production)
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'your_db_name',
        'USER': 'your_db_user',
        'PASSWORD': 'your_db_password',
        'HOST': 'localhost',
        'PORT': '5432',
    }
}
```

### Common Issues & Solutions

1. **Database Migration Issues**
```bash
# Reset migrations
python manage.py migrate --fake
python manage.py makemigrations
python manage.py migrate --fake-initial

# If database is corrupted
rm db.sqlite3
python manage.py migrate
```

2. **Static Files Issues**
```bash
# Force collect static files
python manage.py collectstatic --noinput --clear
```

3. **Virtual Environment Problems**
```bash
# If venv is not working
deactivate  # If already in a venv
rm -rf venv
python -m venv venv
```

## 🔧 Development Workflow

1. **Running Tests**
```bash
python manage.py test
```

2. **Creating Admin User**
```bash
python manage.py createsuperuser
```

3. **Accessing Admin Panel**
- Go to: http://127.0.0.1:8000/admin
- Login with superuser credentials

## 📋 Project Structure
```
Job-Portal-Django/
├── accounts/          # User authentication
├── jobs/              # Job listings and applications
├── static/            # CSS, JavaScript, Images
├── templates/         # HTML templates
├── media/            # User uploaded files
└── manage.py         # Django management script
```

## 🖼️ Screenshots

<details>
<summary>Click to view screenshots</summary>

### Home Page
![Home Page](https://raw.github.com/Sany07/Django-Job-Portal/master/screenshots/screencapture-127-0-0-1-8000-2020-05-08-17_03_46.png)

### Jobs List
![Jobs List](https://raw.github.com/Sany07/Django-Job-Portal/master/screenshots/screencapture-127-0-0-1-8000-jobs-2020-05-08-17_40_01.png)

### Job Details
![Job Details](https://raw.github.com/Sany07/Django-Job-Portal/master/screenshots/screencapture-127-0-0-1-8000-job-79-2020-05-08-16_59_55.png)

### Job Creation
![Job Creation](https://raw.github.com/Sany07/Django-Job-Portal/master/screenshots/screencapture-127-0-0-1-8000-job-create-2020-05-08-17_00_46.png)

### Dashboard
![Dashboard](https://raw.github.com/Sany07/Django-Job-Portal/master/screenshots/screencapture-127-0-0-1-8000-dashboard-2020-05-08-17_01_07.png)

### Applicants View
![Applicants](https://raw.github.com/Sany07/Django-Job-Portal/master/screenshots/screencapture-127-0-0-1-8000-dashboard-employer-job-54-applicants-2020-05-08-17_01_34.png)

</details>

## 🚦 Application Status Codes

- 200: Success
- 400: Bad Request
- 401: Unauthorized
- 403: Forbidden
- 404: Not Found
- 500: Server Error

## 📝 License

This project is open-source and available under the MIT License.

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check [issues page](https://github.com/Manikanta1239/Job-Portal-Django/issues).

---

<div align="center">
    <p>If you found this project helpful, please consider giving it a ⭐️</p>
</div>

