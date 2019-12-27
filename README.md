# Basic-Django-Login-Registration-System
<br/>

##### How to Use
> This repo is a simple login/registraction system that comes from Corey Schafer's youtube series on Django. I recommend that you take a look at his series in order to understand what is going on and how it all works. To implement this system into your own Django project, follow the instructions below.
1. Update project Settings file
   * Add the users app to installed apps: `'users.apps.UserConfig'`
   * Add login redirect url to end of settings file: `LOGIN_REDIRECT_URL = '<your-redirect-url-of-choice>'`
   * Add login url to end of settings file: `LOGIN_URL = 'login'`
2. Edit extension clause in templates
   * Each template extends a base template and you will need to edit this clause in order to fit your needs. Change this line in each template to extend from your projects base template: `{% extends "main/base.html" %}`
3. Add the users app urls to your main project urls.py file.
   * `path('', include('users.urls'))`
4. Make migrations and migrate your changes and you should be ready to go.

> Now that you have the app ready to use, you can add in your links to your base template or where ever needed to allow users to register and login to your website. To ensure that users are logged in to view a specific page, you would use the `@login_required` decorator on function based views and the `LoginRequiredMixin` mixin for class based views.

> If yon notice any issues, just submit a new issue or pull request, and I will try to find a fix or merge in fixes.
