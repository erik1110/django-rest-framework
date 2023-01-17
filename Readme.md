# Django-Rest-Framework

## Creae Your Project

### Start up
```
django-admin startproject <your project name>
```

### Add rest_framework
./demo/demo/settings.py
```
INSTALLED_APPS = [
    ...
    'rest_framework',
]
```

### Run Server

```
python3 manage.py runserver
```

## DB 
In Django, the makemigrations and migrate commands are used to manage the database schema and data for your application.

`makemigrations` is used to generate migration files based on the changes you have made to your models. These migration files contain instructions for creating, altering, or deleting database tables, fields, and indexes to match the current state of your models.

`migrate` command is used to apply the changes described in the migration files to the actual database. This command creates or modifies the database tables, fields, and indexes to match the current state of the models, and it also updates the database schema version in the django_migrations table.

When you make changes to your models, you need to use the makemigrations command to create new migration files and then use the migrate command to apply these changes to the database.

```
# Generates migration files based on the changes in models.py
python3 manage.py makemigrations

# Applies the changes to the database
python3 manage.py migrate
```

## Serializers

Serializers are used to ensure that the data sent to and received from the client is in a consistent format, and that the data is valid. They also provide a way to easily convert data between the internal representation used by the application and the external representation used by the client.

Add ./demo/user/serializers.py for user


### Note

FastAPI and Flask are web frameworks that can be used to build web applications and APIs. Both frameworks have their own way of handling data and validation, and they do not include built-in support for serializers like Django REST framework does.

FastAPI uses Pydantic library to handle input and output data validation, it provide a way to define and validate the data models, Pydantic provide a lot of features that are similar to serializers like validating the input data, handling the input data, changing the data type and etc.

Flask does not provide a built-in way to handle data validation and serialization, but there are many libraries that can be used with Flask to handle this. For example, the Flask-Marshmallow library provides support for serializing and deserializing data using the Marshmallow library, which is similar to Django REST framework's serializers.

In summary, both FastAPI and Flask do not have built-in support for serializers like Django REST framework does. However, you can use third-party libraries like Pydantic or Flask-Marshmallow to handle data validation and serialization in FastAPI and Flask respectively.