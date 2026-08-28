## Project Origin

This project is based on and modified from [full_stack-flask_shop_template](https://github.com/fchavonet/full_stack-flask_shop_template) by **fchavonet**.

All rights to the original code belong to the original author. See the Modifications section below for what was changed.

## Modifications

Added full Docker support to run the project:

- **Dockerfile**: builds a dedicated image for the Flask app based on Python 3.12
- **docker-compose.yml**: orchestrates two services:
  - `flask` (the app itself)
  - `mysql` (database, replacing manual local setup)
  - Internal Docker network linking both services
  - Persistent volume for MySQL data
  - Healthcheck to ensure the database is ready before the app starts
- **requirements.txt**: added PyMySQL for MySQL connectivity
- **run.py**: adjusted for compatibility with the Docker environment
- **.gitignore**: updated to exclude unnecessary files from the repository

The goal of these changes is to let the project run locally with a single command, without manually installing Python or MySQL on the host machine.

