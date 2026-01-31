# Django Task Management CRUD

A simple Django CRUD (Create, Read, Update, Delete) application for managing tasks efficiently.

## Features

- ✅ **Create Tasks** - Add new tasks with title, description, priority, and due date
- 📖 **Read Tasks** - View all tasks or individual task details
- ✏️ **Update Tasks** - Edit existing tasks and update their status
- 🗑️ **Delete Tasks** - Remove completed or unwanted tasks
- 🔍 **Filter** - Filter tasks by status (Pending, In Progress, Completed)
- 💾 **Priority Levels** - Set task priority (1=Low, 2=Medium, 3=High)
- 📅 **Due Dates** - Assign due dates to track deadlines
- 🎨 **Bootstrap UI** - Responsive and modern user interface

## Project Structure

```
tempcurd/
├── manage.py                 # Django management script
├── taskmanager/             # Main Django project
│   ├── settings.py          # Project settings
│   ├── urls.py              # URL configuration
│   └── wsgi.py              # WSGI configuration
├── tasks/                   # Tasks app
│   ├── models.py            # Task model
│   ├── views.py             # CRUD views
│   ├── forms.py             # Task form
│   ├── urls.py              # App URLs
│   ├── admin.py             # Django admin configuration
│   ├── migrations/          # Database migrations
│   └── templates/           # HTML templates
│       └── tasks/
│           ├── base.html
│           ├── task_list.html
│           ├── task_detail.html
│           ├── task_form.html
│           └── task_confirm_delete.html
├── requirements.txt         # Python dependencies
└── README.md               # This file
```

## Installation

### 1. Clone or navigate to the project directory
```bash
cd /home/tush/jbproject/tempcurd
```

### 2. Create a virtual environment
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

### 4. Run migrations
```bash
python manage.py migrate
```

### 5. Create a superuser (optional, for admin access)
```bash
python manage.py createsuperuser
```

### 6. Run the development server
```bash
python manage.py runserver
```

The application will be available at `http://127.0.0.1:8000/`

## Usage

### Main Views
- **Task List** (`/`) - View all tasks with filtering options
- **Task Detail** (`/task/<id>/`) - View detailed information about a task
- **Create Task** (`/task/new/`) - Create a new task
- **Edit Task** (`/task/<id>/edit/`) - Update an existing task
- **Delete Task** (`/task/<id>/delete/`) - Delete a task

### Admin Panel
Access the Django admin panel at `/admin/` to manage tasks directly.

## Task Model

The Task model includes:
- **Title** (CharField) - Task name
- **Description** (TextField) - Detailed task description
- **Status** (CharField) - Pending, In Progress, or Completed
- **Priority** (IntegerField) - 1 (Low), 2 (Medium), 3 (High)
- **Due Date** (DateTimeField) - Task deadline
- **Created At** (DateTimeField) - Task creation timestamp
- **Updated At** (DateTimeField) - Last modification timestamp

## Technologies Used

- **Django 4.2+** - Web framework
- **SQLite** - Database
- **Bootstrap 5** - Frontend framework
- **Python 3.11+** - Programming language

## Future Enhancements

- User authentication and task ownership
- Task categories/tags
- Task reminders and notifications
- Recurring tasks
- Task assignment to multiple users
- Comment/activity tracking
- Export tasks to CSV/PDF
- API endpoints for mobile apps
# lg2
