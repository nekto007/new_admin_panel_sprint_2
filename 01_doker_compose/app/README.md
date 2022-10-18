# Project assignment: admin panel

You need to develop a service that will allow you to create and edit records in the database.

Readiness criteria:

- The admin panel interface is configured with standard Django tools.
- It allows you to create, edit and delete movies, genres and personas.
- Links between movies, genres and personas are created on the movie editing page.
- You are using the database created in the previous step.
- Django system tables do not use the content schema.
- You have described an initial migration that creates the same structures as SQL from the first task.
- Tables are described in the models.py file.
- `settings.py` is split into logical modules
- Created and modified fields are filled in automatically.
- Sensitive data is taken from environment variables
- All texts translated into Russian using `gettext_lazy`

## First start

1) Create a virtual Python environment
2) Install job dependencies `pip install -r requirements`
3) Install pre-commit hook `pre-commit install` (for development)

## Linter

Used by `flake8`.

The configuration is in `setup.cfg`

Run: `flake8`