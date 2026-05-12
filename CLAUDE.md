# Global Art Gallery

A multilingual Flask web application serving as a solo portfolio piece for a CERN internship application, forked and improved from a group college project.

## Stack

- **Framework:** Flask
- **i18n:** Flask-Babel (English, Chinese `zh_CN`, Japanese `ja_JP`)
- **Database (target):** PostgreSQL via SQLAlchemy
- **Deployment:** Render with Gunicorn (`Procfile` already present)
- **Dependencies:** `requirements.txt`

## Key Files

- `__init__.py` — app factory / configuration
- `routes.py` — URL routing and view logic
- `artistdata.py` — artist and painting data (currently Python dicts, migrating to PostgreSQL)
- `templates/` — Jinja2 templates

## Data Layer

Artist and painting data currently lives in `artistdata.py` as plain Python dictionaries. The planned migration is to PostgreSQL with SQLAlchemy models replacing those dicts.

## Planned Improvements

- Migrate `artistdata.py` to PostgreSQL with SQLAlchemy
- Fix hardcoded secret key (move to environment variable)
- Rewrite README
- Delete the stub `/art` page
- Add server-side form validation
- Add basic pytest tests
