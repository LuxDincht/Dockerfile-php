# PHP Symfony

Image PHP Docker afin de pouvoir faire du Symfony avec les librairies :
- intl
- imagemagick
- mbstring
- pdo_mysql
- zip
- unzip
- dnsutils
- opcache
- **composer**
- **xdebug**
- apcu

## Usage

### Ligne de Commande

```bash
docker run --rm --env-file .env -v web:/project/html -v tmp:/tmp sephilux/php:latest
```

(ou)

```bash
docker run --rm --env-file .env -v web:/project/html sephilux/php:latest [PARAM_COMMAND_PHP]
```

### Docker-compose

```docker-compose.yml
version: '3'

services:
  php:
    image: sephilux/php:latest
    env_file:
      - .env
    volumes:
      - ${PWD}/web:/project/html
      - ${PWD}/tmp:/tmp
```
