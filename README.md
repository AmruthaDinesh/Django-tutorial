# Django-tutorial

# Django installation


1. Open Command Prompt and Type:

    ```sh
    #This command helps create a setup for the environment
    pip install virtualenvwrapper-win
    ```

2. Create a virtual environment
    ```sh
    #To create a virtual environment
    mkvirtualenv env_name
    ```

3. Activate the virtual environment and then install django using the command
    ```sh
    #To install django
    pip install django
    ```

    ***And Django is installed succesfully in your virtual environment!***

4. Run the following command to check the version
    ```sh
    #To check the version installed
    django-admin --version
    ```


# Setting up the django project

1. Create a folder `projects` and move into that folder
    ```sh
    #Command to create the project
    django-admin startproject project_name
    ```

2. Go inside the directory you just created using the above command
    ```sh
    cd project_name
    ```
3. Run the server!
    ```sh
    #It helps to check if the installation was succesful
    python manage.py runserver      
    ```

# Now What? Create a django app

1. Go to cmd (Don't forget to activate the virtual environment)
    ```sh
      #This command helps create a django app 'app_name_here'
      python manage.py startapp app_name_here        
    ```

2. Inside the `app_name_here` create a file `urls.py`


# Day 2

1. Create a folder templates

    * Inside templates create a `home.html` file.
    * Add some basic contents inside `home.html`
    * But the page will not be available at http://127.0.0.1:8000/
    * To make it available we need to go to the `views.py` file and create the following function:
        ```py
          def home(request):
              return render(request,"home.html")
        ```
      * Then go to `settings.py` and in the `TEMPLATES` we add this `DIRS: [os.path.join(BASE_DIR,'templates')]`

        So it should look something like below code snippet
        ```py
          TEMPLATES={
          'BACKEND': 'django.template.backends.django.DjangoTemplates',
                'DIRS': [os.path.join(BASE_DIR,'templates')],
                'APP_DIRS': True,
                'OPTIONS':....
                .....
                .....
          }
        ```

      * Then go to `urls.py` of `app_name` and then add the following
        ```py
          urlpatterns= [
            path('', views.home, name='home')
          ]
        ```
    
    
    
# Next

# Still incomplete , come back later


