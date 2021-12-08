# Django Vite Example

Example of using [Django Vite](https://github.com/MrBin99/django-vite) module into a basic Django project.

# Advice

- This is a really basic example to help people figure out how to setup the module.
- Don't use this project as is.
- Use it as an helper to begin with and build your configuration upon it.

# How to Use:

Follow these steps to set up:

```shell
# 1. Clone repo
git clone https://github.com/MrBin99/django-vite-example

# 2. Make Python Virtual Env
cd django-vite-example
python -m venv .venv
# 3. Install python requirements

pip install django django-vite whitenoise

# OR

poetry install

# 4. install Vite requirements
yarn
```

### For Development servers:
```shell
# in one terminal run:
python manage.py runserver

# in another terminal run:
yarn dev
```

Navigate to [http://127.0.0.1:8000/](http://127.0.0.1:8000/) and see the cool words.

### For Production Simulation:

in `settings.py`:
```python
# set Debug = false
Debug = False
```

then:
```shell
yarn prod
python manage.py collectstatic
python manage.py runserver
```

Static files created by vite, collected by Django will be served by [WhiteNoise](http://whitenoise.evans.io/en/stable/index.html)