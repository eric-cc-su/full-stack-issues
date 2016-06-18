## **Django**

**TIP**: Make sure you set `DEBUG = True` in your settings file if you're testing on your local environment

### Internal Server Error

Obviously this has many implications and with debug set to False it can be tough to figure out the exact problem. Some things to try are:

1. Make sure `ALLOWED_HOSTS` in your settings file includes your server name, as well as `localhost` or whatever IP you're using for testing while debug is False.

### 'No module named...' on startup

If you're using virtual environments make sure you activated the environment before you try starting the django
development server. This is as simple as calling `. /dir/to/env/activate` on the command line (for UNIX systems)

### 'No module named...' elsewhere

It is convenient to have a "requirements.txt" file that keeps track of the modules that your environment needs. If 
you're getting a "no module named..." error, check if the module is listed in your requirements and add it if it's not. 
Then try installing the module with pip or another appropriate package manager. 

UNIX: `sudo pip install module`

### Static Files Issues

- Make sure STATIC_URL in your settings file(s) is properly set. Typically to `/static/`
- Check that your templates call on your static files with `{% load staticfiles %}` at the top of the file
- Make sure you're not accidentally including your STATIC_URL in your HTML links (e.g. `href="static/css/file.css"`)

[Django docs](https://docs.djangoproject.com/en/1.9/howto/static-files/)

### MySQL errors

If you've made any changes to your models you will have to make and apply 
[django migrations](https://docs.djangoproject.com/en/1.9/topics/migrations/) to update your MySQL tables
unless you have a custom configuration.

- make migrations - `python manage.py makemigrations`
- apply migrations - `python manage.py migrate`
