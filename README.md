# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

Include your ER diagram here

![image](https://github.com/mithra916/django-orm-app/assets/149986612/6d018421-2ae3-4c40-b0c9-350de42d8823)

## DESIGN STEPS
Write your own steps
### STEP 1:
Clone the repository in ex02 from github
### STEP 2:
Move to project directory where manage.py is located and create newapp in Django project (python3 manage.py startapp myapp)
### STEP 3:
Then, change necessary things in settings.py and add the required codes to models.py and admin.py
### STEP 4:
Then, migrate the codes using the required command and run the server.

## PROGRAM
Include your code here
### CODE FROM MODELS.PY:
```
from django.db import models
from django.contrib import admin
class Football(models.Model):
    player_name=models.CharField(max_length=20)
    age=models.IntegerField()
    email=models.EmailField()
class FootballAdmin(admin.ModelAdmin):
    list_display=('player_name','age','email')
```
### CODE FROM ADMIN.PY:
```
from django.contrib import admin
from .models import Football,FootballAdmin
admin.site.register(Football,FootballAdmin)
```
## OUTPUT
PLAYER DETAILS

![Screenshot 2024-01-29 190335](https://github.com/mithra916/django-orm-app/assets/149986612/64748bac-bcf9-4af7-ab84-de3fb1582a73)

## RESULT
Thus the program for creating the database using Django ORM has been executed successfully.
