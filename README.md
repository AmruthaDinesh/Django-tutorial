# Django-tutorial

# Django installation


Open Command Prompt and Type :

pip install virtualenvwrapper-win          #This command helps create a setup for the environment

mkvirtualenv env_name                      #To make the virtual environment

Activate the virtual environment and then install django using the command

pip install django

and django is installed succesfully.(in the virtual environment)

django-admin --version                   #check the version

# Setting up the django project

Create a folder 'projects' and move into that folder

django-admin startproject project_name      #command to create the project

cd project_name

python manage.py runserver  #it helps check if the installation was succesful

# Now What? Create a django app

Go to cmd (Don't forget to activate the virtual environment)

python manage.py startapp app_name_here        #this command helps create a django app 'app_name_here'

inside the 'app_name_here' create a file urls.py


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


