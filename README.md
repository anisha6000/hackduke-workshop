# hackduke-workshop

Links

* Django
    * https://docs.djangoproject.com/en/2.2/intro/tutorial01/
* Pipenv
    * https://github.com/pypa/pipenv
    * https://thinkdiff.net/python/python-pipenv-tutorial-%F0%9F%94%A5-how-to-install-in-windows-and-mac-%F0%9F%8E%AF/
* Heroku Django Config
    * https://devcenter.heroku.com/articles/django-app-configuration
* Heroku CLI Install
    * https://devcenter.heroku.com/articles/heroku-cli#download-and-install
* Heroku Getting Started
    * https://github.com/heroku/python-getting-started.git


Instructions

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
7. SOOOO let's make it live!
    1. pipenv install django-heroku
8. in the settings.py let's add the import and run
    1. import django_heroku
    2. django_heroku.settings(locals())
9. let's setup some source control (code repo) on GitHub
    1.  
10. ... and get your local setup too, in your folder in terminal type 
    1. git init
    2. git remote add origin https://github.com/KineticHub/hackduke-workshop
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
13. now we do something similar, except that we set it up for Heroku
    1. brew tap heroku/brew && brew install heroku