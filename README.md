
  
## Installation
1. Clone the repository:
```
git clone https://my-personal-portfolio.git
```
2. Navigate to the project directory:
```
cd `django-tailwind-blog`
```
3. Create and activate a new virtual environment:
```
python -m venv env
source env/bin/activate
```
4. Install the project dependencies:
```
pip install -r requirements.txt
```
5. Install the `django-tailwind` module:
```
pip install django-tailwind
```
6. Add `tailwind` to your `INSTALLED_APPS` list in `settings.py`:
```python
INSTALLED_APPS = [
    # ...
    'tailwind',
    # ...
]
```
7. Run the Tailwind CSS configuration command:
```python
python manage.py tailwind init
```
8. Create the database tables:
```python
python manage.py migrate
```
9. Run the development server:
```python
python manage.py runserver
```

## Technologies used
1. HTML
2. CSS
3. JavaScript
4. Python

### Primary Modules used
1. Django==4.1.4
2. django-tailwind==3.4.0
3. whitenoise==6.3.0
4. psycopg2==2.9.5
5. django-tinymce==3.5.0

## Features
1. Responsive design using Tailwind CSS
2. Admin dashboard for managing blog posts and portfolio items
3. Contact form for sending messages to the site owner

## Pages
- `Home`: The landing page of the website, which displays a brief introduction and links to other pages.
- `About`: A page that provides information about the site owner, their background, and skills.
- `Contact`: A page that contains a contact form for visitors to send messages to the site owner.
- `Blog`: A page that displays a list of blog posts in reverse chronological order, with links to individual post pages.
- `Blog Post`: A page that displays the content of a single blog post, including the title, author, date, and content.
- `Projects`: A page that displays a list of portfolio projects, with links to individual project pages.
- `Project`: A page that displays the details of a single portfolio project, including the title, description, date, and any relevant images or links.
- `Categories`: A page that displays a list of blog post categories, with links to filtered lists of posts for each category.
- `Custom 404 Pages`: Custom error pages that display when a user navigates to a non-existent page or encounters an error.


## Deployment
To deploy this project to a web server, you can follow these general steps:

1. Set up a web server that can run Python applications. This could be a VPS, a PaaS like Heroku, or a cloud-based server like AWS.
2. Clone the repository to your server:
```
git clone https://my-personal-portfolio.git
```
3. Install the project dependencies on your server using `pip`:
```
pip install -r requirements.txt
```
4. Set up a database for the project, if necessary. You can use a database like PostgreSQL, MySQL, or SQLite, depending on your needs.
5. Configure the settings.py file with your server's settings:
```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'mydatabase',
        'USER': 'mydatabaseuser',
        'PASSWORD': 'mypassword',
        'HOST': 'localhost',
        'PORT': '5432',
    }
}

STATIC_ROOT = '/var/www/static/'
MEDIA_ROOT = '/var/www/media/'

ALLOWED_HOSTS = ['example.com', 'www.example.com']
```
The DATABASES setting specifies the database connection details. In this example, we're using PostgreSQL with a database named `mydatabase`, a user named `mydatabaseuser`, and a password of `mypassword`. The `STATIC_ROOT` and `MEDIA_ROOT` settings specify the file paths where static files and media files will be stored. The `ALLOWED_HOSTS` setting is a list of domain names that the application is allowed to serve.
6. Run the python manage.py collectstatic command to collect all the static files into the STATIC_ROOT directory:
```python
python manage.py collectstatic
```
7. Start the Django development server, or set up a production server using a WSGI server like uWSGI or Gunicorn.
```python
python manage.py runserver
```
8. Access the website using your server's IP address or domain name, and the port number of the server if necessary. For example, if you're running the development server on port 8000, you can access the website at `http://your-server-ip:8000/`.
