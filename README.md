# Cookiecutter Django Fun

Just a simple [cookiecutter](http://cookiecutter.readthedocs.org/) template for small Django projects and having some fun.
It creates a project managed with [pipenv](https://pipenv.pypa.io/en/latest/):

- `Pipenv` and `Pipenv.lock` so that you can just run `pipenv install`
- [pre-commit](https://pre-commit.com/) configuration so that you can just run `pre-commit install`

It has a Django project layout based on the one described by "Two Scoops of Django 3.x":

```
.
├── LICENSE.txt
├── Pipfile
├── Pipfile.lock
├── README.md
├── config
│   ├── __init__.py
│   ├── asgi.py
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
├── manage.py
└── project_slug
    └── main_app
        ├── __init__.py
        ├── admin.py
        ├── apps.py
        ├── migrations
        │   └── __init__.py
        ├── models.py
        ├── tests.py
        └── views.py
```

That way, you just need to run the following:

```
pre-commit install
pipenv install
```

And now you can start developing the app.
For example, you can run the following without issues:

```
pipenv run python manage.py runserver
```

## Usage

Install cookiecutter with:

```
python -m pip install cookiecutter
```

Clone this project:

```
git clone git@github.com:manugrandio/cookiecutter-django-fun.git
```

Create project based on this cookiecutter template:

```
cookiecutter cookiecutter-django-fun
```

Then, follow the steps described in the `README.md` of the project you just generated.

## Pending additions

- `pytest` support
- `coverage` support
