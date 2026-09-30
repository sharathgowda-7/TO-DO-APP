# TO-DO-APP

# To-Do App

A small Flask application for managing tasks through a simple web interface.

## Features

- Login and logout flow
- Add new tasks
- Move tasks through `pending`, `working`, and `done` statuses
- Clear all tasks
- SQLite database storage through Flask-SQLAlchemy

## Requirements

- Python 3.9 or newer
- Flask
- Flask-SQLAlchemy

## Installation

From the project root:

```powershell
python -m venv venv
venv\Scripts\Activate.ps1
pip install Flask Flask-SQLAlchemy
```

If PowerShell blocks activation, run the commands from an activated Python environment or use the equivalent activation command for your shell.

## Run the application

```powershell
python run.py
```

Open http://127.0.0.1:5000 in a browser.

The SQLite database is created automatically when the application starts. It is stored in Flask's instance directory.

## Demo login

```text
Username: sharath
Password: 2944
```

These credentials are currently hard-coded for demonstration purposes. Change them and move authentication to a secure user store before using the application in production.

## Project structure

```text
run.py                  Application entry point
app/
	__init__.py           Flask application factory and database setup
	models.py             User and Task database models
	routes/
		auth.py             Login and logout routes
		tasks.py            Task management routes
	static/               CSS and JavaScript assets
	templates/            Jinja HTML templates
instance/               Local SQLite database files
```

## Task status flow

New tasks start as `pending`. Selecting **next** changes the status to `working`, then to `done`.
