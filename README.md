# Django Deployment


## Feature
- Django
- Gunicorn
- Pipenv

## Setting up local enviornment
```bash
$ PIPENV_VENV_IN_PROJECT=true pipenv install --three
Creating a virtualenv for this project…
Pipfile: /Users/kim.hyunsung/django/pipenv-django/Pipfile
Using /usr/local/opt/python/bin/python3.7 (3.7.2) to create virtualenv…
⠴ Creating virtual environment...Already using interpreter /usr/local/opt/python/bin/python3.7
Using base prefix '/usr/local/Cellar/python/3.7.2_1/Frameworks/Python.framework/Versions/3.7'
New python executable in /Users/kim.hyunsung/django/pipenv-django/.venv/bin/python3.7
Also creating executable in /Users/kim.hyunsung/django/pipenv-django/.venv/bin/python
Installing setuptools, pip, wheel...
done.

✔ Successfully created virtual environment!
Virtualenv location: /Users/kim.hyunsung/django/pipenv-django/.venv
Creating a Pipfile for this project…
Installing django…
⠙ Installing...
Adding django to Pipfile's [packages]…
✔ Installation Succeeded
Pipfile.lock not found, creating…
Locking [dev-packages] dependencies…
Locking [packages] dependencies…
✔ Success!
Updated Pipfile.lock (4f9dd2)!
Installing dependencies from Pipfile.lock (4f9dd2)…
  🐍   ▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉ 2/2 — 00:00:01
To activate this project's virtualenv, run pipenv shell.
Alternatively, run a command inside the virtualenv with pipenv run.
```

## Use virtual environment
```
$ pipenv shell
Launching subshell in virtual environment…
 . /Users/kim.hyunsung/django/pipenv-django/.venv/bin/activate

~/django/pipenv-django at ☸️  minikube 
➜  . /Users/kim.hyunsung/django/pipenv-django/.venv/bin/activate

~/django/pipenv-django via pipenv-django at ☸️  minikube 
➜ 

```

## Create project and getting Start server
```
$ django-admin.py startproject hello_django .
$ python manage.py migrate
Operations to perform:
  Apply all migrations: admin, auth, contenttypes, sessions
Running migrations:
  Applying contenttypes.0001_initial... OK
  Applying auth.0001_initial... OK
  Applying admin.0001_initial... OK
  Applying admin.0002_logentry_remove_auto_add... OK
  Applying admin.0003_logentry_add_action_flag_choices... OK
  Applying contenttypes.0002_remove_content_type_name... OK
  Applying auth.0002_alter_permission_name_max_length... OK
  Applying auth.0003_alter_user_email_max_length... OK
  Applying auth.0004_alter_user_username_opts... OK
  Applying auth.0005_alter_user_last_login_null... OK
  Applying auth.0006_require_contenttypes_0002... OK
  Applying auth.0007_alter_validators_add_error_messages... OK
  Applying auth.0008_alter_user_username_max_length... OK
  Applying auth.0009_alter_user_last_name_max_length... OK
  Applying sessions.0001_initial... OK

$ python manage.py runserver
Performing system checks...

System check identified no issues (0 silenced).
March 05, 2019 - 20:28:22
Django version 2.1.7, using settings 'hello_django.settings'
Starting development server at http://127.0.0.1:8000/
Quit the server with CONTROL-C.
[05/Mar/2019 20:28:27] "GET / HTTP/1.1" 200 16348
[05/Mar/2019 20:28:27] "GET /static/admin/css/fonts.css HTTP/1.1" 200 423
[05/Mar/2019 20:28:27] "GET /static/admin/fonts/Roboto-Regular-webfont.woff HTTP/1.1" 200 80304
[05/Mar/2019 20:28:27] "GET /static/admin/fonts/Roboto-Bold-webfont.woff HTTP/1.1" 200 82564
[05/Mar/2019 20:28:27] "GET /static/admin/fonts/Roboto-Light-webfont.woff HTTP/1.1" 200 81348
Not Found: /favicon.ico
```