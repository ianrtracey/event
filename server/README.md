# Setup Instructions


## Install pipenv
Install it from (here)[https://github.com/pypa/pipenv].
Then:
```
pipenv install 3.7.1
```


## Install Poetry
Install it from (here)[https://github.com/sdispater/poetry].
Then:
```
poetry install
```

## Install system dependencies
sudo apt install postgresql postgresql-contrib libpq-dev


## Running
Make sure to set the following env variables
```
export FLASK_ENV=development
export DATABASE_URL=postgres://name:password@host:port/blog_api_db
export JWT_SECRET_KEY=hhgaghhgsdhdhdd
poetry shell
python run.py

# hit endpoints with:
wget -qO - http://localhost:5000/ 
```


## Database
# Installation
Make sure to install and run postgres >= 11.xx


# Migration
to create the tables
`python manage.py db init`

to create the migration changes for the db
`python manage.py db migrate`

to apply the changes to the db
`python manage.py db upgrade`
