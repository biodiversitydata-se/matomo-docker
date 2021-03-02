# matomo-docker

A dockerized Matomo instance .

Copy `./env/matomo.template` to `./env/matomo.env` and edit to set credentials for database.

The `proxy` service section has been commented out to use external reverse proxy in production.

Uncomment to run it locally.

Uses external network `sbdinet` in production which can be created by

`docker network create sbdinet`

The volume `matomo_data` needs to be served using webserver/reverse proxy.

```
volumes:
  - matomo_data:/var/www/html
```
