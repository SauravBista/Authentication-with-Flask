Flask Authentication App

This is a Flask web application that includes user registration, login, and authentication functionalities. The app allows users to sign up, log in, view secret content, and download files, all secured by user authentication.

Features

- User Registration: New users can sign up with an email, name, and password.
- User Login: Registered users can log in using their email and password.
- Password Hashing: User passwords are securely hashed using werkzeug.security.generate_password_hash.
- User Authentication: Only authenticated users can access the secret page and download files.
- Logout: Users can securely log out of the application.

Technologies Used

- Flask: A micro web framework for Python.
- Flask-SQLAlchemy: An extension for Flask that adds support for SQLAlchemy.
- Flask-Login: Manages user sessions and handles user login/logout.
- Werkzeug Security: Provides utilities for securely hashing and verifying passwords.
- SQLite: A lightweight, disk-based database used to store user data.

Setup

1. Clone the repository:
    git clone https://github.com/yourusername/flask-authentication-app.git
    cd flask-authentication-app

2. Create and activate a virtual environment:
    python3 -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`

3. Install the dependencies:
    pip install -r requirements.txt

4. Run the application:
    python app.py

5. Access the app:
    Open your web browser and go to http://127.0.0.1:5000/.

Project Structure

.
├── app.py                  # Main application file
├── templates               # HTML templates
│   ├── index.html
│   ├── register.html
│   ├── login.html
│   ├── secrets.html
├── static                  # Static files (CSS, JS, images, etc.)
│   └── files
│       └── cheat_sheet.pdf
└── users.db                # SQLite database file

Routes

- /: Home page.
- /register: User registration page.
- /login: User login page.
- /secrets: Secret page accessible only to logged-in users.
- /logout: Log out the current user.
- /download: Download the secret file, accessible only to logged-in users.

License

This project is licensed under the MIT License - see the LICENSE file for details.
