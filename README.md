# Microblog

A microblogging website written in Flask where users can create accounts, share posts, and much more.

## Features

- User authentication (sign up, log in, log out)
- Create, edit, and delete posts
- View posts from other users
- Flash messages for user feedback
- CSRF protection

## Installation

1. **Clone the repository:**
    ```sh
    git clone https://github.com/theroycode/microblog.git
    cd microblog
    ```

2. **Create a virtual environment:**
    ```sh
    python3 -m venv venv
    source venv/bin/activate
    ```

3. **Install the dependencies:**
    ```sh
    pip install -r requirements.txt
    ```

4. **Set up the database:**
    ```sh
    flask db init
    flask db migrate -m "Initial migration"
    flask db upgrade
    ```

5. **Run the application:**
    ```sh
    flask run
    ```

## Configuration

The application configuration is managed in the `config.py` file. You can set environment variables to override the default settings.

## Deployment

To deploy the application to Heroku, follow these steps:

1. **Install Heroku CLI:**
    Download and install the Heroku CLI from the [Heroku Dev Center](https://devcenter.heroku.com/articles/heroku-cli).

2. **Create a `Procfile`:**
    ```sh
    echo "web: flask run --host=0.0.0.0 --port=\$PORT" > Procfile
    ```

3. **Create a `requirements.txt`:**
    ```sh
    pip freeze > requirements.txt
    ```

4. **Create a `runtime.txt`:**
    ```sh
    echo "python-3.9.6" > runtime.txt
    ```

5. **Initialize a Git repository:**
    ```sh
    git init
    git add .
    git commit -m "Initial commit"
    ```

6. **Create a Heroku app:**
    ```sh
    heroku login
    heroku create your-app-name
    ```

7. **Deploy to Heroku:**
    ```sh
    git push heroku master
    ```

8. **Open your app:**
    ```sh
    heroku open
    ```

## License

This project is licensed under the MIT License. See the `LICENSE` file for more details.