# [Soft UI Design System](https://appseed.us/ui-kit/soft-ui-design-system) Flask

**[Soft UI Design System](https://appseed.us/ui-kit/soft-ui-design-system)** is a Premium Bootstrap 5 UI Kit designed by [Creative-Tim](https://bit.ly/3fKQZaL) designed for those who like bold elements and beautiful websites. **Soft UI Design System Flask**  is a simple Flask starter provided by AppSeed with a modular codebase, database, authentication and deployment scripts - Features:

<br />

- UI Kit: **Soft UI Design System** (Free Version) by **Creative-Tim**
- SQLite database, Flask-SQLAlchemy ORM
- Session-Based auth flow (login, register)
- Deployment scripts: Docker, Gunicorn / Nginx, Heroku
- Support via **Github** (issues tracker) and [Discord](https://discord.gg/fZC6hup).

<br />

> Links

- [Soft UI Design System Flask](https://appseed.us/product/flask-soft-ui-design-system) - product page
- [Soft UI Design System Flask - Demo](https://flask-soft-ui-free.appseed-srv1.com/) - LIVE Deployment

<br />

## Want more? Go PRO!

PRO versions include **Premium UI Kits**, Lifetime updates and **24/7 LIVE Support** (via [Discord](https://discord.gg/fZC6hup))

| [Flask Soft UI PRO](https://appseed.us/product/flask-soft-ui-pro) | [Flask Material PRO](https://appseed.us/admin-dashboards/flask-dashboard-material-pro) | [Flask Volt PRO](https://appseed.us/admin-dashboards/flask-dashboard-volt-pro) |
| --- | --- | --- |
| [![Flask Soft UI PRO](https://raw.githubusercontent.com/app-generator/soft-ui-design-system/main/media/soft-ui-design-system-screen.png)](https://appseed.us/product/flask-soft-ui-pro) | [![Flask Material PRO](https://raw.githubusercontent.com/app-generator/flask-dashboard-material-pro/master/media/flask-dashboard-material-pro-screen.png)](https://appseed.us/admin-dashboards/flask-dashboard-material-pro) | [![Flask Volt PRO](https://raw.githubusercontent.com/app-generator/flask-dashboard-volt-pro/master/media/flask-dashboard-volt-pro-screen.png)](https://appseed.us/admin-dashboards/flask-dashboard-volt-pro)

<br />
<br />

![Flask Template - Starter provided by AppSeed.](https://raw.githubusercontent.com/app-generator/flask-soft-ui-free/master/media/flask-soft-ui-free-screen.png)

<br />

## Build from sources

```bash
$ # Clone the sources
$ git clone https://github.com/app-generator/flask-soft-ui-free.git
$ cd flask-soft-ui-free
$
$ # Virtualenv modules installation (Unix based systems)
$ virtualenv env
$ source env/bin/activate
$
$ # Virtualenv modules installation (Windows based systems)
$ # virtualenv env
$ # .\env\Scripts\activate
$
$ # Install requirements
$ pip3 install -r requirements.txt
$
$ # Set the FLASK_APP environment variable
$ (Unix/Mac) export FLASK_APP=run.py
$ (Windows) set FLASK_APP=run.py
$ (Powershell) $env:FLASK_APP = ".\run.py"
$
$ # Set up the DEBUG environment
$ # (Unix/Mac) export FLASK_ENV=development
$ # (Windows) set FLASK_ENV=development
$ # (Powershell) $env:FLASK_ENV = "development"
$
$ # Run the application
$ # --host=0.0.0.0 - expose the app on all network interfaces (default 127.0.0.1)
$ # --port=5000    - specify the app port (default 5000)  
$ flask run --host=0.0.0.0 --port=5000
$
$ # Access the app in browser: http://127.0.0.1:5000/
```

> Note: To use the app, please access the registration page and create a new user. After authentication, the app will unlock the private pages.

<br />

## Code-base structure

The project has a super simple structure, represented as bellow:

```bash
< PROJECT ROOT >
   |
   |-- app/__init__.py
   |-- app/
   |    |-- static/
   |    |    |-- <css, JS, images>         # CSS files, Javascripts files
   |    |
   |    |-- templates/
   |    |    |
   |    |    |-- includes/                 # Page chunks, components
   |    |    |    |
   |    |    |    |-- navigation.html      # Top bar
   |    |    |    |-- sidebar.html         # Left sidebar
   |    |    |    |-- scripts.html         # JS scripts common to all pages
   |    |    |    |-- footer.html          # The common footer
   |    |    |
   |    |    |-- layouts/                  # App Layouts (the master pages)
   |    |    |    |
   |    |    |    |-- base.html            # Used by common pages like index, UI
   |    |    |    |-- base-fullscreen.html # Used by auth pages (login, register)
   |    |    |
   |    |    |-- accounts/                 # Auth Pages (login, register)
   |    |    |    |
   |    |    |    |-- login.html           # Use layout `base-fullscreen.html`
   |    |    |    |-- register.html        # Use layout `base-fullscreen.html`  
   |    |    |
   |    |  index.html                      # The default page
   |    |  page-404.html                   # Error 404 page (page not found)
   |    |  page-500.html                   # Error 500 page (server error)
   |    |    *.html                        # All other pages provided by the UI Kit
   |
   |-- requirements.txt
   |
   |-- run.py
   |
   |-- ************************************************************************
```

<br />

## Deployment

The app is provided with a basic configuration to be executed in [Docker](https://www.docker.com/), [Heroku](https://www.heroku.com/), [Gunicorn](https://gunicorn.org/), and [Waitress](https://docs.pylonsproject.org/projects/waitress/en/stable/).

<br />

### [Docker](https://www.docker.com/) execution
---

The application can be easily executed in a docker container. The steps:

> Get the code

```bash
$ git clone https://github.com/app-generator/flask-soft-ui-free.git
$ cd flask-soft-ui-free
```

> Start the app in Docker

```bash
$ sudo docker-compose pull && sudo docker-compose build && sudo docker-compose up -d
```

Visit `http://localhost:5005` in your browser. The app should be up & running.

<br />

### [Heroku](https://www.heroku.com/)
---

Steps to deploy on **Heroku**

- [Create a FREE account](https://signup.heroku.com/) on Heroku platform
- [Install the Heroku CLI](https://devcenter.heroku.com/articles/getting-started-with-python#set-up) that match your OS: Mac, Unix or Windows
- Open a terminal window and authenticate via `heroku login` command
- Clone the sources and push the project for LIVE deployment

```bash
$ # Clone the source code:
$ git clone https://github.com/app-generator/flask-soft-ui-free.git
$ cd flask-soft-ui-free
$
$ # Check Heroku CLI is installed
$ heroku -v
heroku/7.25.0 win32-x64 node-v12.13.0 # <-- All good
$
$ # Check Heroku CLI is installed
$ heroku login
$ # this commaond will open a browser window - click the login button (in browser)
$
$ # Create the Heroku project
$ heroku create
$
$ # Trigger the LIVE deploy
$ git push heroku master
$
$ # Open the LIVE app in browser
$ heroku open
```

<br />

### [Gunicorn](https://gunicorn.org/)
---

Gunicorn 'Green Unicorn' is a Python WSGI HTTP Server for UNIX.

> Install using pip

```bash
$ pip install gunicorn
```
> Start the app using gunicorn binary

```bash
$ gunicorn --bind 0.0.0.0:8001 run:app
Serving on http://localhost:8001
```

Visit `http://localhost:8001` in your browser. The app should be up & running.

<br />

### [Waitress](https://docs.pylonsproject.org/projects/waitress/en/stable/)
---

Waitress (Gunicorn equivalent for Windows) is meant to be a production-quality pure-Python WSGI server with very acceptable performance. It has no dependencies except ones that live in the Python standard library.

> Install using pip

```bash
$ pip install waitress
```
> Start the app using [waitress-serve](https://docs.pylonsproject.org/projects/waitress/en/stable/runner.html)

```bash
$ waitress-serve --port=8001 run:app
Serving on http://localhost:8001
```

Visit `http://localhost:8001` in your browser. The app should be up & running.

<br />

## [Soft UI Design System](https://appseed.us/ui-kit/soft-ui-design-system) - UI Kit

Most complex and innovative Design System Made by Creative Tim. Soft UI Design System is built with over 70 frontend individual elements, like buttons, inputs, navbars, navtabs, cards or alerts, giving you the freedom of choosing and combining. All components can take variations in colour, that you can easily modify using SASS files and classes.

You will save a lot of time going from prototyping to full-functional code, because all elements are implemented. This Free Bootstrap 5 UK Kit is coming with prebuilt design blocks, so the development process is seamless, switching from our pages to the real website is very easy to be done.

<br />

## Credits & Links

- [Flask Framework](https://www.palletsprojects.com/p/flask/) - The official website
- [Boilerplate Code](https://appseed.us/boilerplate-code) - Index provided by **AppSeed**
- [Boilerplate Code](https://github.com/app-generator/boilerplate-code) - Index published on Github

<br />

---
[Soft UI Design System](https://appseed.us/ui-kit/soft-ui-design-system) Flask - Provided by **AppSeed** [App Generator](https://appseed.us/app-generator).
