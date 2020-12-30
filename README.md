# ART Real Estate: A Description

ART Real Estate is a full-stack web application that provides role-based management and search of real estate listings and realtors.  The technology stack includes Python, Django, Postgresql, Jinja, and Bootstrap. The application is deployed to Digital Ocean and served via Gunicorn and Nginx. 


## User Stories

- As an administrator, I would like to post new real estate listings with descriptions and images.
- As an administrator, I would like to edit existing real estate listings.
- As an administrator, I would like to post new realtors with images.
- As an administrator, I would like to edit existing realtors.
- As an administrator, I would like to assign a featured realtor the title of "Realtor of the Month."
- As an administator, I would like to receive emails when a customer makes an inquiry on a property.
- As a customer, I would like to view all listings and realtors.
- As a customer, I would like to filter listings by specifications (price, bedrooms, description keywords, location, etc.)
- As a customer, I would like to create an account and sign in.
- As a signed-in customer, I would like to make an inquiry about a listing.
- As a signed-in customer, I would like to view all of my past listing inquiries.

## API End Points

| Verb   | URI Pattern                    | Description                       |
|--------|--------------------------------|-----------------------------------|
| GET    | `/`                            | `homepage`                        | 
| GET    | `/admin`                       | `admin portal`                    |
| GET    | `/about`                       | `about`                           |
| GET    | `/listings`                    | `all listings`                    |
| GET    | `/listings/<int:listing_id>`   | `individual listing`              |
| GET    | `/listings/search          `   | `listings that match search`      |
| GET    | `/accounts/register`           | `view registration form`          |
| POST   | `/accounts/register`           | `send registration credentials`   |
| GET    | `/accounts/login`              | `view sign in form`               |
| POST   | `/accounts/login`              | `send sign in credentials`        |
| GET    | `/accounts/dashboard`          | `view list of existing inquiries` |
| POST   | `/accounts/logout`             | `log out of account`              |
| POST   | `/contact`                     | `send inquiry`                    |

`PATCH` and `DELETE` methods for listings, accounts, and contacts only available to users with administrator privileges.

## Planning Story

- [Gantt Chart](https://docs.google.com/spreadsheets/d/1xvZ6CXHSKE_Q4nan2bH51XatrNw7pyXpcjKPrnNClT8/edit?usp=sharing)

## Set Up Instructions
- Open the PSQL shell with `psql`.
- Create a new database for the project with `CREATE DATABASE <your_database_name>;`.
- Exit PSQL shell with `/q`.
- Fork and clone this repository.
- Once inside the directory, start the virtual environment with `pipenv shell`.
- Run `pipenv install` to install dependencies.
- Initialize the database with `python3 manage.py makemigrations` followed by `python3 manage.py migrate`.
- Run the development server with `python3 manage.py runserver`.
- The application will run on `http://localhost:8000/` in the browser.
- Create a user with admin privileges with `python3 manage.py createsuperuser`.
- Log into the Django admin portal with your credentials at `http://localhost:8000/admin`.



### Technologies Used

- Python
- Django
- PostgresQL
- Jinja
- HTML
- CSS
- Bootstrap

## Images

#### Screenshot:

![Screenshot](https://user-images.githubusercontent.com/67024033/103311919-2dcfe280-49e1-11eb-876d-a47c1edb59be.png)
