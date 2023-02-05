#### Description:
### ToDo - WebApp
A simple WebApp that allows registered users to manage their tasks.

#### Technologies used:
HTML
<br>
CSS
<br>
Python
<br>
sqlite3
<br>
Flask
<br>
other small libraries
<br>

#### How the webpage works?
The idea is simple. The user can register and login to use it.
<br>
Username: During registration it is checked if the username is not taken.
<br>
Password: During registration it is checked to match and hashed before storing.
<br>

#### Sessions
The webpage uses sessions to confirm that user is registered.
<br>

#### Database
Database stores all users and their tasks.
<br>
<br>
/static
<br>
CSS file
<br>
Size for brand, Colors for brand
<br>
todo icon
<br>
<br>
/templates
<br>
add.html (a form where user submits task, description and deadline)
<br>
Add a task
<br>
apology.html (return apology with a cat image)
<br>
Ref - https://memegen.link/
<br>
contact.html (contact info)
<br>
index.html (loop over and show tasks from database for each user)
<br>
If there is no task, there will be 'add a task' button and a heading "A fresh start!"
<br>
If there are tasks, there will be a table with columns "Task, Description, Assigned and Deadline"
<br>
layout.html (default layout for all templates)
<br>
Ref - http://getbootstrap.com/docs/5.1/
<br>
If user is not logged in, there will be register and login links on navbar.
<br>
If user is logged in, there will be contact and logout links on navbar.
<br>
get_flashed_messages() purpose is to alert user.
<br>
login and register (a form where user submits username and password)
<br>
<br>
app.py - (python file with flask)
<br>
Imports:
<br>
SQL from cs50
<br>
Flask, flash, redirect, render_template, request, session from flask
<br>
Session from flask_session
<br>
mkdtemp from tempfile
<br>
check_password_hash, generate_password_hash from werkzeug.security
<br>
import apology, login_required from helpers
<br>
<br>
Configure application
<br>
Ensure templates are auto-reloaded
<br>
Configure session to use filesystem (instead of signed cookies)
<br>
Configure CS50 Library to use SQLite database
<br>
<br>
Functions:
<br>
after_request(response)
<br>
Ensure responses aren't cached.
<br>
index()
<br>
Show tasks
<br>
add()
<br>
Add new task
<br>
delete()
<br>
Delete all tasks
<br>
contact()
<br>
Contact info
<br>
login()
<br>
Log user in
<br>
logout()
<br>
Log user out
<br>
register()
<br>
Register user
<br>
helpers.py - (a helper function where apology() and login_required() are defined)
<br>
<br>
tasks.db - (sqlite3 database with users and data tables)