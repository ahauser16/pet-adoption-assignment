# Pet Adoption Exercise - Table of Contents

- [Pet Adoption Exercise - Table of Contents](#pet-adoption-exercise---table-of-contents)
  - [Project Overview](#project-overview)
  - [How to use this application](#how-to-use-this-application)
    - [Installation](#installation)
    - [running the application:](#running-the-application)
    - [psql and the database:](#psql-and-the-database)
    - [How to use `flask_migrate`](#how-to-use-flask_migrate)

## Project Overview 

[Back to TOC](#notarious---table-of-contents)

## How to use this application

### Installation

[Back to TOC](#notarious---table-of-contents)

Provide detailed instructions on how to install your project. For example:

1. `pip install -r requirements.txt`

2. There is a virtual environment already set up for this project so you need to activate it:

`source venv/bin/activate`

3. In `Flask`, the `FLASK_APP` environment variable is used to specify how to load the application which can be set to a python file, a module, or a package. In this case, it's being set to the `app.py` file which is where my `Flask` application is defined. When you execute the command `flask run`, `Flask` uses the value of `FLASK_APP` to find my application and run it. If `FLASK_APP` is not set, `Flask` won't know where the application is and won't be able to run it. So before you run the application you must run the command:

`export FLASK_APP=app.py`

4. Now you can run the application with the debugger module activated using the command:

`flask run --debugger`

### running the application:

[Back to TOC](#notarious---table-of-contents)

1. There is a virtual environment already set up for this project so you need to activate it:

`source venv/bin/activate`

2. In Flask, the `FLASK_APP` environment variable is used to specify how to load your application. It can be set to a python file, a module, or a package. In this case, it's being set to the `app.py` file, which is presumably where your Flask application is defined.

When you run `flask run`, Flask uses the value of `FLASK_APP` to find your application and run it. If `FLASK_APP` is not set, Flask won't know where your application is and won't be able to run it. So before you run the application you must run the command:

`export FLASK_APP=app.py`

3. Now you can run the application:

`flask run --debugger`

### psql and the database:

[Back to TOC](#notarious---table-of-contents)

1. Since this is a Unix-based system you must activate the PostgreSQL service with the command:
   NB--> be prepared to enter your `psql` password

`sudo service postgresql start`

2. To log in to your PSQL account you must use the `psql` command with the `-U` option followed by your username:

`psql -U your_username`

### How to use `flask_migrate`

To generate a migration script and update your data models using Flask-Migrate, follow these steps:

1. Generate Migration Script: This command auto-generates a migration script from the detected changes in the models.

`flask db migrate -m "Your message here"`

Replace "Your message here" with a brief description of the changes or additions you've made to your models.

2. Apply the Migration: This command applies the changes specified in the migration script to the database.

`flask db upgrade`

Ensure you have Flask-Migrate installed and properly configured in your Flask application before running these commands.
