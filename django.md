# Django Framework

> Replace `[this]` with suitable value.

## Installing django

`$ pip3 install django djangoframework`

## Creating new project

`$ django-admin startproject [project_name]`

## Creating new app

`$ django-admin startapp [app_name]`

## Running live server

`$ python3 manage.py runserver`

## Creating or Updating/Syncing database

> Creates database. Updates/Migrate the database with new models.  

`$ python3 manage.py makemigrations`

`$ python3 manage.py migrate`

## Checking SQL code before migrate

> Migration number is visible at [app_name]\migrations

`$ python3 manage.py sqlmigrate [app_name] [migration_number]`

## Object relational mappers to sql

> app_name is the application name and generated file number is generated

`$ python3 manage.py sqlmigrate [app_name] [generated_file_number]`

## Creating super user or admin

> Must create a database and migrate before creating a superuser

`$ python3 manage.py createsuperuser`

## Quering the database

### Running shell

`$ python3 manage.py shell`

### Importing models

`$ from [app].models import [model]`

`$ from django.contrib.auth.models import User`

### Quering model from db (`__str__()` to change what to return when retrieving and exit the shell and restart)

`$ [model].objects.all()`

`$ [model].object.first()`

`$ [model].object.last()`

`$ [model].objects.filter(fieldname='..')`

`$ [model].objects.filter(fieldname='..').first()`

`$ [model_var] = [model].objects.filter(fieldname='..')`

`$ [model_var].id`

`$ [model_var].email`

`$ [model_var].pk`

`$ [model_var] = [model].objects.get(id=..)`

### Creating model instance

`$ [model_var2] = model(fieldname='..', fieldname='..', fieldname='..')`

`$ [model_var2].save()`

`$ [model_var3] = [model].objects.first()`

`$ [model_var3].fieldname`

### Here model_var3.fieldname returns a models instance (post.author.email)

`$ [model_var3].fieldname.[returned_models_fieldname]`

### Finding two models common instance

`$ [model1] = [model1].objects.filter(fieldname1='')`

`$ [model2] = model2.objects.filter(fieldname2 = model1.fieldname3)`

`$ [model1].model2_set`

`$ [model1].model2_set.all()`

`$ [model1].model2_set.create(model2_fieldname1='', model2_filedname='')`

## Other commands

> The following commands can be in the blank space. `python3 manage.py ______`

- `check`
- `compilemessages`
- `createcachetable`
- `dbshell`
- `diffsettings`
- `dumpdata`
- `flush`
- `inspectdb`
- `loaddata`
- `makemessages`
- `makemigrations`
- `migrate`
- `runserver`
- `sendtestemail`
- `shell`
- `showmigrations`
- `sqlflush`
- `sqlmigrate`
- `sqlsequencereset`
- `squashmigrations`
- `startapp`
- `startproject`
- `test`
- `testserver`
