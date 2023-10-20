



#### Check Django Version
py -m django --version

#### Django Project Creation
1) django-admin startproject project_name
2) manage.py: start server from here
3) __init__.py: to tell that this is a python project
4) settings.py: all info related to db, authentication, etc
5) urls.py: all urls that should be matched with incoming url.
6) wsgi.py: 

#### Run Django
1) python manage.py runserver
2) you can replace 127.... with localhost

#### Views.py
1) creates user based info in views.py file
2) python manage.py startapp app_name

#### Run app
1) YOU HAVE 18 UNAPPLIED MIGRATIONS WARNING
2) python manage.py migrate 
3) Migrate - Create database tables as per the scripts

#### Build own database
1) Create Model in the models.py in the app
2) in settings.py add the food.apps.FoodConfig
3) run the migrate - python manage.py makemigrations food
4) python manage.py sqlmigrate food 0001
5) python manage.py migrate

#### Storing data in the database
1) Database Abstraction API
2) Create, Update and Delete object 
3) Use the Interactive Shell to write into database
4) python manage.py shell

``` 
from food.models import Item
Item.objects.all()
a= Item()
a= Item(item_name="Pizza", item_desc="cheesy pizz", item_pricey=900)
a.save()
a.id or a.pk


```

7) Follow shell way or admin way

#### Django Admin Panel and Creating Super User
1) python manage.py createsuperuser
2) enter username and password
3) python manage.py runserver
4) Edit admin.py - Models u want to display in admin panel should be edited here

#### Retrieve Data from Database
1) Queryset, Manager, Model
2) Model - Item database - all()
3) Queryset - collection of objects in databse
4) Manager - to pull data from query set. (object)


### Templates in Django
1) Basically Django has its own template by default in settings.py

#### Django Template Language (DTL)
1) templating engine?
2) Jinja2, DTL (default)
3) remove hardcoded urls - 
4) Namespacing - add app_name in urls.py
5) and rename all urls to food:detail

### Static files and site design
