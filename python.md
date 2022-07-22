# Python: Creating Environment

## Creating new directory

`$ mkdir [project_name]`

## Changing to that directory

`$ cd [project_name]`

## Creating environment

`$ python3 -m venv [enviroment_name]`

`$ py -3 -m venv [enviroment_name]`

> `venv` or `env` is the most common name for environment.

## Activating environment

`$ . [enviroment_name]/bin/activate`

`$ [enviroment_name]\Scripts\activate`

## Print installed packages

`$ pip list`

## Installing dependencies from requirements.txt

`$ pip install -r requirements.txt`

## Creating requirements.txt

`$ pip freeze > requirements.txt`

> Virutal environment package is not available in python 2
