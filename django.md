## **Django**

**TIP**: Make sure you set `DEBUG = True` in your settings file if you're testing on your local environment

### 'No module named...' on startup

If you're using virtual environments make sure you activated the environment before you try starting the django
development server. This is as simple as calling `. /dir/to/env/activate` on the command line (for UNIX systems)

### 'No module named...' elsewhere

It is convenient to have a "requirements.txt" file that keeps track of the modules that your environment needs. If 
you're getting a "no module named..." error, check if the module is listed in your requirements and add it if it's not. 
Then try installing the module with pip or another appropriate package manager. 

UNIX: `sudo pip install module`

### MySQL errors

If you've made any changes to your models you will have to make and apply 
[django migrations](https://docs.djangoproject.com/en/1.9/topics/migrations/) to update your MySQL tables
unless you have a custom configuration.

- make migrations - `python manage.py makemigrations`
- apply migrations - `python manage.py migrate`
