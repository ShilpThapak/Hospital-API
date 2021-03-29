# Hospital-API

## Endpoints

Here is the list of endpoints available in the app. Use these endpoints after **api/v1/**. For instance if you want to get a list of beds go to http://127.0.0.1:8000/api/v1/.

| Endpoints                         | HTTP Verb |
|-----------------------------------|-----------|
| /                                 | GET       |
| /:pk                              | GET       |
| /bookings                         | GET       |
| /bookings/create                  | POST      |
| /bookings/:pk                     | GET       |
| users/                            | GET       |
| users/:pk/                        | GET       |
| /rest-auth/registration           | POST      |
| /rest-auth/login                  | POST      |
| /rest-auth/logout                 | GET       |
| /rest-auth/password/reset         | POST      |
| /rest-auth/password/reset/confirm | POST      |

## Installation Instructions

### Activate virtual environment

Create a virtual environment and activate it.

### Install Dependencies

Use the following command in the terminal to install all the dependencies from requirement.txt file.

pip install -r requirements.txt

### Setup MongoDB Database

Go to MongoDB compass and create a new database. Remember the name of the database to update database settings.

Go to settings.py and change the database settings. Replace the &#39;NAME&#39; field with the name of your database.


DATABASES = {

&#39;default&#39;: {

&#39;ENGINE&#39;: &#39;djongo&#39;,

&#39;NAME&#39;: &#39;database\_name&#39;,

}

}

### Migrate

Run the following commands in terminal to migrate to database and start the server.

Python manage.py migrate

Python manage.py runserver
