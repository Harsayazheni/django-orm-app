# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram
![photo_2022-12-18_08-54-46](https://user-images.githubusercontent.com/118708467/208279960-252821cf-91ea-4aef-ba3d-4445870e176b.jpg)


## Design Steps
### STEP 1:

Create a new Django project using  "django-admin startproject",get into the project terminal  and use "python3 manage.py startapp" command.
 
### STEP 2:

Define a model for the golf club membership in the models.py.Allow host access and add the app name under installed apps in settings.py

### STEP 3:

Register the models with the Django admin site. In admin.py under app folder,register the models with Django admin site.


### STEP 4:

Run the python manage.py makemigrations and python manage.py migrate commands to create the necessary database tables for the golf club membership model.Run the Server using "python3 manage.py runserver 0:80" command.


## PROGRAM

#IN models.py:-
```
from django.db import models
from django.contrib import admin

# Create your models here.
class Instagrampage(models.Model):
    member_id = models.CharField(max_length=8,primary_key=True)
    name =models.CharField(max_length=100)
    phone_number = models.IntegerField()
    email = models.EmailField()
    membership_type = models.CharField(max_length=100)
    validity = models.IntegerField()

class Instagrampage(admin.ModelAdmin):
    list_display = ('member_id','name','phone_number','membership_type','validity')
 ```

#IN admin.py:-
```
from django.contrib import admin
from .models import Instagrampage,InstagrampageAdmin

admin.site.register(Instagrampage,InstagrampageAdmin)
```

## OUTPUT

![Harsayazheni 22006873 (6)_page-0001 (2)](https://user-images.githubusercontent.com/118708467/215144983-9737ddc2-79a9-49c0-b2f7-01bd40a65ca9.jpg)


## RESULT
Successfully developed a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).
