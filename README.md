## Passport Guide Part I - Authorization Server Example

This is an example application for [Part I of the Passport guide series](https://mattallan.me/posts/passport-guide-auth-server/).

Either follow along with the guide to build your own application, or if you would prefer to use this server as a starting point and skip to part II of the guide, follow the setup steps below.

## Setup

1. Clone the repo.

```
git clone git@github.com:matt-allan/passport-guide-server.git
cd passport-guide-server
```

2. Install dependencies.

```
composer install
```

3. Copy the example .env file.

```
cp .env.example .env
```

4. Generate an app key.

```
php artisan key:generate --ansi
```

5. Create the database. If you prefer a different database use the client of your choice and update the .env file accordingly.

```
mysql -u root -e 'create database passport_server'
```

6. Run the migrations.

```
php artisan migrate
```

7. Setup the domain. If using something besides Valet such as Homestead consult the docs.

```
valet link passport
```