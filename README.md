# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram
![photo_2022-12-18_08-54-46](https://user-images.githubusercontent.com/118708467/208279960-252821cf-91ea-4aef-ba3d-4445870e176b.jpg)



## DESIGN STEPS

### STEP 1:

### STEP 2:

### STEP 3:

Write your own steps

## PROGRAM
#IN models.py:-

from django.db import models
from django.contrib import admin

class GolfClubMember(models.Model):
    member_id = models.CharField(max_length=8,primary_key=True)
    name =models.CharField(max_length=100)
    phone_number = models.IntegerField()
    email = models.EmailField()
    membership_type = models.CharField(max_length=100)
    validity = models.IntegerField()

class GolfClubAdmin(admin.ModelAdmin):
    list_display = ('member_id','name','phone_number','membership_type','validity')
#IN admin.py:-

from django.contrib import admin
from .models import GolfClubMember,GolfClubAdmin

admin.site.register(GolfClubMember,GolfClubAdmin)


## OUTPUT

![Harsayazheni 22006873 (6)_page-0001 (2)](https://user-images.githubusercontent.com/118708467/215144983-9737ddc2-79a9-49c0-b2f7-01bd40a65ca9.jpg)


## RESULT
Successfully developed a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).
