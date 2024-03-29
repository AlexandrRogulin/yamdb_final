# yamdb_final
yamdb_final


[![Yamdb-app workflow](https://github.com/AlexandrRogulin/yamdb_final/workflows/Yamdb-app_workflow/badge.svg)](https://github.com/AlexandrRogulin/yamdb_final/actions)

# API Yamdb Group Project

This is group project from Yandex.Praktikum provided API for multi-user blogging platform divided by categories, genres with ability to add posts, reviews, comments etc.

## Getting Started

Clone repository from GitHub
```sh
$ git clone https://github.com/AlexandrRogulin/yamdb_final.git
$ cd yamdb_final
```
### Prerequisites

Install docker [https://docs.docker.com/get-docker/](https://docs.docker.com/get-docker/) and docker-compose [https://docs.docker.com/compose/install/](https://docs.docker.com/compose/install/)

### Installing

Create ```.env``` file with environment PostreSQL settings and secret key.

```
DB_NAME=
POSTGRES_USER=
POSTGRES_PASSWORD=
DB_HOST=
DB_PORT=
SECRET_KEY=
```

Build and run containers
```
docker-compose up --build -d
```
Log in ```web``` container
```
docker-compose exec web bash
```
Migrate and seed sample data
```
python manage.py migrate --noinput
python manage.py loaddata fixtures.json
```
Create super user
```
python manage.py createsuperuser
```
Log out from container
```
exit
```

*Site is working on your-ip-address:8000/admin*

## Running the tests
```
python -m venv venv
source venv/Scripts/activate
pip install -r requirements.txt
pytest
```
## Technologies

**Django** [https://www.djangoproject.com/](https://www.djangoproject.com/)<br>
**Django Rest Framework** [https://www.django-rest-framework.org/](https://www.django-rest-framework.org/)<br>
**PostgreSQL** [https://www.postgresql.org/](https://www.postgresql.org/)<br>
**Docker** [https://www.docker.com/](https://www.docker.com/)

## Authors

* **Rogulin Alexandr** - [AlexandrRogulin](https://github.com/AlexandrRogulin)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
[MIT License](https://mit-license.org/)

An example of a working api can be viewed at:

http://84.201.176.219/redoc

http://84.201.176.219/admin

