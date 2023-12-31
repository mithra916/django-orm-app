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

# Create your models here.
class Student (models.Model):
    referencenumber=models.CharField(primary_key=True,max_length=20,help_text="reference number")
    name=models.CharField(max_length=100)
    age=models.IntegerField()
    email=models.EmailField()


class StudentAdmin(admin.ModelAdmin):
    list_display=('referencenumber','name','age''email')
```
### CODE FROM ADMINS.PY:
```
from django.contrib import admin
from .models import Student,StudentAdmin


# Register your models here.
admin.site.register(Student,StudentAdmin)
```
## OUTPUT
STUDENTS DETAILS:

![image](https://github.com/mithra916/django-orm-app/assets/149986612/3d4c9342-75ae-4b89-8a24-91f3941620a1)

ERROR:

![image](https://github.com/mithra916/django-orm-app/assets/149986612/43c3d7f6-aa61-4026-b94b-5e9622c26dac)

## RESULT
Thus the program for creating the database using Django ORM has been executed successfully.
