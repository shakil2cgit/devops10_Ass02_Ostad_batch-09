# Django Todo App

A complete Todo web application built with Django, featuring a modern UI with Tailwind CSS.

## Features

- ✅ Create, Read, Update, and Delete tasks
- ✅ Mark tasks as completed/active
- ✅ Filter tasks by status (All, Active, Completed)
- ✅ Set due dates for tasks
- ✅ Add descriptions to tasks
- ✅ AJAX toggle completion without page reload
- ✅ Beautiful, responsive UI with Tailwind CSS
- ✅ Django messages framework for user feedback

## Tech Stack

- **Backend**: Python + Django
- **Frontend**: Django Templates + Tailwind CSS (via CDN)
- **Database**: SQLite (for local development)
- **JavaScript**: Minimal JS for enhanced UX (toggle completion)

## Setup Instructions

### Prerequisites

- Python 3.8 or higher
- pip (Python package manager)

### Installation

1. **Clone or navigate to the project directory:**
   ```bash
   cd /path/to/todo_project
   ```

2. **Create a virtual environment (recommended):**
   ```bash
   python3 -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run migrations:**
   ```bash
   python manage.py migrate
   ```

5. **Create a superuser (optional, for admin access):**
   ```bash
   python manage.py createsuperuser
   ```

6. **Run the development server:**
   ```bash
   python manage.py runserver
   ```

7. **Open your browser and navigate to:**
   ```
   http://127.0.0.1:8000/
   ```

## Project Structure

```
todo_project/
├── manage.py
├── requirements.txt
├── README.md
├── db.sqlite3          # SQLite database (created after migrate)
├── todo_project/       # Project settings
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   ├── wsgi.py
│   └── asgi.py
├── tasks/              # Tasks app
│   ├── __init__.py
│   ├── models.py       # Task model
│   ├── views.py        # CRUD views
│   ├── forms.py        # Task form
│   ├── urls.py         # App URLs
│   ├── admin.py
│   ├── tests.py        # Unit tests
│   └── migrations/     # Database migrations
└── templates/          # HTML templates
    ├── base.html
    └── tasks/
        ├── task_list.html
        ├── task_form.html
        └── task_confirm_delete.html
```

## Usage

### Creating a Task

1. Click the "+ New Task" button on the task list page
2. Fill in the task title (required)
3. Optionally add a description and due date
4. Click "Create Task"

### Managing Tasks

- **View Tasks**: All tasks are displayed on the home page
- **Filter Tasks**: Use the tabs (All/Active/Completed) to filter tasks
- **Toggle Completion**: Click "Mark Complete" or "Mark Active" to toggle task status
- **Edit Task**: Click the "Edit" button to modify a task
- **Delete Task**: Click the "Delete" button and confirm deletion

### Admin Interface

Access the Django admin panel at `http://127.0.0.1:8000/admin/` (requires superuser account).

## Running Tests

```bash
python manage.py test
```

## Development

### Making Changes

1. **Model Changes**: After modifying `models.py`, run:
   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```

2. **Static Files**: This project uses Tailwind CSS via CDN, so no static file collection is needed for development.

## Live Deployment

🚀 **The application is live and publicly accessible at:**

🔗 **[https://devops10-ass02-ostad-batch-09.onrender.com/](https://devops10-ass02-ostad-batch-09.onrender.com/)**

### Deployment Details

| Detail | Info |
|--------|------|
| **Hosting Provider** | Render |
| **Runtime** | Python 3 |
| **WSGI Server** | Gunicorn |
| **Static Files** | WhiteNoise |
| **Database** | SQLite |

### How to Run Locally

1. Clone the repository:
   ```bash
   git clone https://github.com/shakil2cgit/devops10_Ass02_Ostad_batch-09.git
   cd devops10_Ass02_Ostad_batch-09
   ```

2. Create and activate a virtual environment:
   ```bash
   python -m venv venv
   venv\Scripts\activate   # On Windows
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Run migrations:
   ```bash
   python manage.py migrate
   ```

5. Start the development server:
   ```bash
   python manage.py runserver
   ```

6. Open your browser at: `http://127.0.0.1:8000/`

## License

This project is open source and available for educational purposes.
