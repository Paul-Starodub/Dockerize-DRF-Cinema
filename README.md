# Cinema API

---------------------------------------------------------------

API service for cinema management writen on DRF

## Features:

--------------------------------------------------------------
- JWT authenticated:
- Admin panel: /admin/
- Documentation is located at: /api/doc/swagger/
- Managing orders and tickets
- Creating movies with genres and actors
- Creating cinema halls
- Adding movie sessions
- Filtering movies and movie session

---------------------------------------------------------------

## Installing using GitHub

Install PostgresSQL and create db

```shell
git clone https://github.com/Paul-Starodub/Dockerize-DRF-Cinema.git
cd Dockerize-DRF-Cinema
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
````
create .env file with environment variables listed in .env.sample

```shell
python manage.py migrate
python manage.py runserver
```
---------------------------------------------------------------

## Run with docker

Docker should be installed
    
```shell
git clone https://github.com/Paul-Starodub/Dockerize-DRF-Cinema.git
cd Dockerize-DRF-Cinema
docker-compose up
```

### Getting access

You can use following superuser:

- Email: admin@cinema.com
- Password: 1qazcde3

Or create another one by yourself:
- create user via api/user/register/

To work with token use:

- get access token and refresh token via api/user/token/
- verify access token via api/user/token/verify/
- refresh access token via api/user/token/refresh/

#### Note: Make sure to send Token in api urls in Headers as follows

- key: Authorization

- value: Bearer `<token>`

### Cinema API allows:
- via api/admin/ --- Work with admin panel
- via /api/doc/swagger/ --- Detail api documentation by swagger
- via /api/doc/redoc/ --- Detail api documentation by redoc
- via [POST] /api/user/register/ --- Register a new user
- via [POST] /api/user/token/ --- Obtain new Access and Refresh tokens via credential
- via [POST] /api/user/token/refresh/ --- Obtain new Access token via refresh token
- via [POST] /api/user/token/verify/ --- Verify Access token
- via [GET] /api/user/me/ --- Information about user
- via [PUT, PATCH] /api/user/me/ --- Update user information
- via [POST] /api/cinema/genres/ --- Add new genre
- via [GET] /api/cinema/genres/ --- Genres list
- via [GET] /api/cinema/actors/ --- Actors list
- via [POST] /api/cinema/actors/ --- Add new actor
- via [GET] /api/cinema/cinema_halls/ --- Cinema halls list
- via [POST] /api/cinema/cinema_halls/ --- Add new cinema halls list
- via [POST] /api/cinema/movies/ --- Add new movie
- via [GET] /api/cinema/movies/ --- Movies list
- via [GET] /api/cinema/movies// --- Movie detail information
- via [GET] /api/cinema/movie_sessions/ --- Movie sessions list
- via [POST] /api/cinema/movie_sessions/ --- Add new movie session
- via [GET] /api/cinema/movie_sessions// --- Movie session detail information
- via [PUT, PATCH] /api/cinema/movie_sessions// --- Update movie session information
- via [DELETE] /api/cinema/movie_sessions// --- Update movie session information
- via [GET] /api/cinema/orders/ --- Orders list
- via [POST] /api/cinema/orders/ --- Add new order
- via [POST] /api/cinema/orders/ --- Add new order
