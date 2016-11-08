mobile-backend
==============

Django based AWS lambda friendly mobile backend framework. Includes rest framework, bootstrap3

Usage
-----

#. Clone this project
#. Ensure aws/boto credentials are set up with proper access for dev e.g. `~/.aws/credentials`
#. Create virtual environment and install packages `virtualenv venv; source venv/bin/activate; pip install -r requirements.txt`
#. Set up database(s) and migrate with `./manage.py migrate`
#. Create user `./manage.py createsuperuser`
#. Run dev server `./manage.py runserver`
#. Note: for staging/prod, add the `--settings` arg like: `./manage.py createsuperuser --settings mobile_backend.settings.staging`
#. Navigate in browser to `localhost:8000` log in etc. Maybe navigate to `localhost:8000/api` Congrats!
#. Update the setting for SECRET_KEY! This is in `mobile_backend/settings/base.py`. Alternatively you could set DJANGO_SECRET_KEY
#. After making it your own^tm, deploy via zappa. This config is not version controlled! Do not commit it :)::

    zappa init
    zappa deploy staging

Settings
--------

Some settings folks would probably want to change in environment variables/zappa config::

    "AWS_ACCESS_KEY_ID": "key_id",
    "AWS_SECRET_ACCESS_KEY": "secret_key",
    "AWS_STORAGE_BUCKET_NAME": "mobile-backend-bucket",
    "DJANGO_SECRET_KEY": "newly gen'd key",
    "DATABASE_NAME": "mobile_backend",
    "DATABASE_USER": "mobile_backend_user",
    "DATABASE_PASS": "mobile_backend_pass",
    "DATABASE_HOST": "127.0.0.1",
    "DATABASE_PORT": "5432"

License
-------

Copyright (c) 2016 Jon Robison

See included LICENSE for licensing information

