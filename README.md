# hackduke-workshop

Links

* Django
    * https://docs.djangoproject.com/en/2.2/intro/tutorial01/
* Pipenv
    * https://github.com/pypa/pipenv
    * https://thinkdiff.net/python/python-pipenv-tutorial-%F0%9F%94%A5-how-to-install-in-windows-and-mac-%F0%9F%8E%AF/
* Django Rest Framework
    * https://www.django-rest-framework.org/#installation


Instructions

Section 1 - Installation and Local Setup

1. you can use whatever IDE you want, these instructions are agnostic
    1. I personally prefer to use PyCharm (JetBrains) but VSC (Visual Studio Code) is also great
    2. you can use VIM/EMACS/notepad if you are feeling particularly hipster
2. if you want to use a virtual environment, please do so (recommended but outside scope)
    1. brew install pipenv 
    2. or just use regular pip install
3. create the folder you want to work in and go into it
4. here create a requirements.txt file or run pipenv install
    1. pipenv install django
5. create a django project using the django-admin cli
    1. pipenv run django-admin startproject workshop
    2. django-admin startproject workshop
6. now we can run a dev server! wow, gg2ez
    1. pipenv run python manage.py runserver
    2. http://127.0.0.1:8000/
7. update the database with the initial models
    1. pipenv run python manage.py migrate
8. create the database superuser
    1. pipenv run python manage.py createsuperuser
9. create a new respository (source code control) on GitHub
10. then get your local setup too, in your folder in terminal type 
    1. git init
    2. git remote add origin https://github.cloud.capitalone.com/wno983/hackduke-workshop
    3. git remote -v
    4. git pull origin master
11. at this point, I recommend adding things to you .gitignore depending on IDE and system
12. after that update, do the following
    1. git status
        1. what is currently needing to be committed
    2. git add .
        1. adds everything in this directory and subdirectories
    3. git status
        1. notice that they are now ready to be committed
    4. git commit -m "initial django commit"
    5. git push --set-upstream origin master
        1. in the future this is just git push

Section 2 - Adding Django-Rest-Framework (DRF)

1. start by installing the packages needed
    1. pipenv install djangorestframework
    2. pipenv install markdown
    3. pipenv install django-filter
2. update the settings and urls for DRF
3. create a new app to play with
    1. pipenv run django-admin startapp zoo
    2. add the 'zoo' app to the settings.py
3. add some new models and make/migrate them
    1. pipenv run python manage.py makemigrations
    2. pipenv run python manage.py migrate
