# Django Job Portal

A full-featured job portal application built with Django that connects job seekers and employers.

## 📚 Detailed Overview

### For Job Seekers
- Create your professional profile with details including education, experience, and skills
- Upload resume (Supported formats: PDF, DOC, DOCX)
- Search jobs by:
  - Keywords
  - Location
  - Job Type (Full-time, Part-time, Remote, Internship, Freelance)
  - Experience Level
- Track application status (Applied, Under Review, Accepted, Rejected)
- Receive email notifications for application updates and job recommendations

### For Employers
- Company profile management with logo, description, and website
- Post unlimited job listings with details:
  - Job title
  - Job description
  - Required skills
  - Salary range
  - Location options (On-site, Remote, Hybrid)
  - Application deadline
- Review candidate applications with filters
- Download candidate resumes
- Track applicant statistics including number of applicants per job

## ✨ Features

- User authentication (Job Seeker & Employer registration, login, logout, password reset)
- Job posting and management system for employers
- Job applications tracking for job seekers
- Advanced job search and filtering system
- User dashboard for both job seekers and employers
- Responsive and mobile-friendly design
- Email notifications for application updates and job alerts
- Admin panel for site management

## 🔍 Detailed Setup Guide

### Prerequisites Explained

1. **Python 3.8+**
   - Download Python from [python.org](https://www.python.org/)
   - Verify installation:
     ```bash
     python --version
     ```

2. **pip (Python Package Manager)**
   - Should be included with Python installation
   - Verify installation:
     ```bash
     pip --version
     ```

3. **Virtual Environment**
   - Keeps project dependencies isolated and prevents conflicts between projects
   - Create a virtual environment:
     ```bash
     python -m venv venv
     ```
   - Activate virtual environment:
     - **Windows:**
       ```bash
       venv\Scripts\activate
       ```
     - **Linux/Mac:**
       ```bash
       source venv/bin/activate
       ```
   - Verify virtual environment is active:
     ```bash
     which python  # Should point to venv directory
     ```

### Step-by-Step Installation

#### 1. Clone the Repository
```bash
git clone https://github.com/Manikanta1239/Job-Portal-Django.git
cd Job-Portal-Django
```

#### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

#### 3. Configure Database
Edit `settings.py` to set up the database:

- **For SQLite (Default & Easy for Development)**
```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.sqlite3',
        'NAME': BASE_DIR / 'db.sqlite3',
    }
}
```

- **For PostgreSQL (Recommended for Production)**
```python
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

#### 4. Apply Migrations
Migrations are Django’s way of propagating changes you make to your models (such as adding a new field) into your database schema. This step ensures that the database structure aligns with your models.

- Create migration files based on model changes:
  ```bash
  python manage.py makemigrations
  ```
  This command generates migration files inside the `migrations/` directory of each app.

- Apply the migrations to the database:
  ```bash
  python manage.py migrate
  ```
  This updates the actual database schema according to the latest migration files.

- If you encounter issues, try:
  ```bash
  python manage.py migrate --fake-initial
  ```
  This is useful when applying migrations to an existing database that already contains tables.

#### 5. Create Superuser (For Admin Panel Access)
```bash
python manage.py createsuperuser
```
Provide email, username, and password when prompted.

#### 6. Run the Development Server
```bash
python manage.py runserver
```
- Access the site at: `http://127.0.0.1:8000/`
- Admin panel: `http://127.0.0.1:8000/admin`

## 🔧 Development Workflow

1. **Running Tests**
```bash
python manage.py test
```

2. **Managing Static Files**
```bash
python manage.py collectstatic --noinput --clear
```

3. **Deploying to Production**
   - Use Gunicorn and Nginx for a production setup
   - Use PostgreSQL instead of SQLite
   - Enable HTTPS with an SSL certificate

## 📋 Project Structure
```
Job-Portal-Django/
├── accounts/          # User authentication (Job Seekers & Employers)
├── jobs/              # Job listings and applications
├── static/            # CSS, JavaScript, Images
├── templates/         # HTML templates
├── media/             # User uploaded files (Resumes, Profile Pictures)
└── manage.py          # Django management script
```

## 🖼️ Screenshots

<details>
<summary>Click to view screenshots</summary>

### Home Page
![Home Page](https://raw.github.com/Manikanta1239/Job-Portal-Django/master/screenshots/home.png)

### Job Search
![Job Search](https://raw.github.com/Manikanta1239/Job-Portal-Django/master/screenshots/job_search.png)

### Job Details
![Job Details](https://raw.github.com/Manikanta1239/Job-Portal-Django/master/screenshots/job_details.png)

### Employer Dashboard
![Employer Dashboard](https://raw.github.com/Manikanta1239/Job-Portal-Django/master/screenshots/employer_dashboard.png)

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

Contributions, issues, and feature requests are welcome! Feel free to check the [issues page](https://github.com/Manikanta1239/Job-Portal-Django/issues).

---

<div align="center">
    <p>If you found this project helpful, please consider giving it a ⭐️</p>
</div>

