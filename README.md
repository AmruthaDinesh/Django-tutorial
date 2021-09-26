# Django-tutorial

Create a virtual environment say 'myproject'

Now, don't forget to activate it.

To activate :
Open VS code terminal (and select cmd, by default VS code terminal opens powershell)
workon myproject     // this will activate the virtual environment myproject 

Now type the command to install Django in the virtual environment.

pip install django

and django is installed succesfully.(in the virtual environment)

# Now What?

to be updated

# Day 2

Create a folder templates

inside templates:
 create home.html file
 Inside home.html: type something but it wont be available in the url http://127.0.0.1:8000/
 To make it available we go to the views.py file and create a function :
 
 def home(request):
    return render(request,"home.html")
    
  then we go to settings.py and in the TEMPLATES we add 'DIRS' : [os.path.join(BASE_DIR,'templates')]
  
  TEMPLATES={
   'BACKEND': 'django.template.backends.django.DjangoTemplates',
        'DIRS': [os.path.join(BASE_DIR,'templates')],
        'APP_DIRS': True,
        'OPTIONS':....
        .....
        .....
  }
  
  then go to urls.py of app_name and then add
  
  urlpatterns= [
    path('', views.home, name='home')
    ]
    
    
# Next

# Still incomplete , come back later


