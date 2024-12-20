# Wikibase Everywhere

Welcome to the Wikibase Everywhere project! This project aims to provide a simple way to interact with a local wikibase instance.

## Installation

Copy the .env.example to .env and modify the following variables:

```bash
DB_NAME=wikibase
DB_USER=wikibase
DB_PASS=wikibase
```

Note that we use the following host configuration in our config settings, double check `./config/`flder to match the values you use.

```bash
WIKIBASE_PUBLIC_HOST=wikibase.example.com
WDQS_FRONTEND_PUBLIC_HOST=wdqs-frontend.example.com
QUICKSTATEMENTS_PUBLIC_HOST=quickstatements.example.com
```

If you're testing locally, please add the following lines to your `/etc/hosts` file:

```bash
127.0.0.1 wikibase.example.com
127.0.0.1 wdqs-frontend.example.com
127.0.0.1 quickstatements.example.com
``` 

Then run the following commands:

```bash
docker-compose up
```

Thee installation will now copy two files in you r local config folder. Stop docker and modify them:

```bash
docker-compose down
```
e.g. modify the server host in  `./config/LocalSettings.php` according to your configuration:

```php
$wgServer = 'http://wikibase.example.com';
```

## Deploymnet

Deployment is complicated, we delegate it to the Wiki pages...
