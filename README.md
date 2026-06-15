# WorkTrack

A full-stack internal company web application for managing employee tasks, attendance, and team performance — built collaboratively by a two-person team.

---

## Overview

WorkTrack provides two separate experiences based on user role:

**Employees** — manage their own tasks, mark attendance, track performance, and receive notifications for deadlines.

**Managers** — oversee the entire team, assign tasks, review job applications, monitor attendance, and track individual performance.

---

## Features

### Employee
- Kanban board with drag and drop task management
- Attendance calendar with check-in, check-out, and working hours tracking
- Late arrival detection
- Notifications for new tasks, deadlines, and overdue tasks
- Profile page with avatar upload, GitHub and LinkedIn links

### Manager
- Dashboard with team-wide stats — total employees, present today, active tasks, pending applications
- Task assignment with project links and priority levels
- Full team task view — one column per employee
- Attendance table with filters by employee and date, CSV export
- Team performance overview with attendance rate and task completion metrics
- Job application review — approve or reject applicants
- Notifications for missed deadlines, low attendance, completed tasks, and new applications

---

## Tech Stack

| Layer    | Technology                          |
|----------|-------------------------------------|
| Frontend | HTML, CSS, Bootstrap 5, JavaScript  |
| Backend  | Python, Django, Django REST Framework |
| Database | PostgreSQL                          |
| Auth     | JWT (JSON Web Tokens)               |

---

## Pages

| Page | Access |
|------|--------|
| Login | Everyone |
| Register / Apply | Public applicants |
| Dashboard | Employee + Manager (different views) |
| Tasks | Employee + Manager (different views) |
| Attendance | Employee + Manager (different views) |
| Overview | Manager only |
| Applications | Manager only |
| Profile | All logged-in users |
| Notifications | All logged-in users |

---

## Project Structure

```
WorkTrack/
├── API/                    # Django REST API endpoints
├── dev_task_manager/       # Django project settings
├── tasks/                  # Tasks app
├── users/                  # Users and authentication
├── website/                # Frontend templates and static files
│   ├── templates/
│   └── static/
│       ├── css/
│       └── js/
├── media/                  # User uploaded files (not committed)
├── manage.py
├── requirements.txt
└── .env                    # Environment variables (not committed)
```

---

## Getting Started

```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/WorkTrack.git
cd WorkTrack

# Create virtual environment
python -m venv venv

# Activate virtual environment
# Windows:
venv\Scripts\activate
# Mac/Linux:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Set up environment variables
# Create a .env file and add your values (see below)

# Run migrations
python manage.py migrate

# Start server
python manage.py runserver
```

---

## Environment Variables

Create a `.env` file in the root directory:

```
SECRET_KEY=your_django_secret_key
DEBUG=True
DATABASE_URL=your_database_url
ALLOWED_HOSTS=localhost,127.0.0.1
```

---

## Team

| Role               | Name              |
|--------------------|-------------------|
| Frontend Developer | Nasir Ali Soomro  |
| Backend Developer  | Junaid Akhter     |

---

## Status

✅ Deployed and live
