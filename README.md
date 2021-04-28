# Simple template of Stationery shop

92 tests (code coverage - 95%)

configured factories for tests

in accounts app, business logic now in additional file (services.py)

## To launch shop

clone project

create virtual environment
```
python3 -m venv env
```
launch virtual environment
```
. env/bin/activate
```
install dependencies
```
pip install -r requirements.txt
```
in same dir where manage.py, create file .env and place in .env this environment variables with your values:

SECRET_KEY=''

EMAIL_HOST_USER=''

EMAIL_HOST_PASSWORD=''

ADMIN_EMAIL=''

BRAINTREE_MERCHANT_ID=''

BRAINTREE_PUBLIC_KEY=''

BRAINTREE_PRIVATE_KEY=''

PSQL_DATABASE=''

PSQL_USER=''

PSQL_PASSWORD=''

don't forget to install PostgreSQL and change PORT in settings to 5432, or install PgBouncer for PORT 6432

install extension pg_trgm in your PostgreSQL Database (this is for search function)

```
sudo su - postgres
psql your_database
CREATE EXTENSION pg_trgm;
```

## Things to improve

Split requirements for production, development, testing. (Done in Stationery-shop-v02-with-Docker)
Split settings for production, development, testing. (Done in Stationery-shop-v02-with-Docker)
