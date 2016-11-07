mobile-backend
==============

Django based AWS lambda friendly mobile backend framework. Includes rest framework, bootstrap3

Usage
-----

#. Clone this project
#. Ensure aws/boto credentials are set up with proper access e.g. `~/.aws/credentials`
#. Create virtual environment and install packages `virtualenv venv; source venv/bin/activate; pip install -r requirements.txt`
#. Set up database(s) and migrate with `./manage.py migrate --settings mobile_backend.settings.dev`
#. Create user `./manage.py createsuperuser --settings mobile_backend.settings.dev`
#. Run dev server `./manage.py runserver --settings mobile_backend.settings.dev`
#. Navigate in browser to `localhost:8000` log in etc. Maybe navigate to `localhost:8000/api` Congrats!
#. After making it your own^tm, deploy via zappa. This config is not version controlled! Do not commit it :)::

    zappa init
    zappa deploy dev

License
-------

Copyright (c) 2016 Jon Robison

See included LICENSE for licensing information

