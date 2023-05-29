## Export docker-default-platform

`export DOCKER_DEFAULT_PLATFORM=linux/x86_64 `

## Instalar Postgres 

`docker run -d -e POSTGRES_USER=odoo -e POSTGRES_PASSWORD=odoo -e POSTGRES_DB=postgres --platform linux/x86_64 --name db postgres:15`

## Instalar odoo y linkear con la carpeta de addons y con la carpeta de la configuracion

`docker run -d -v <ruta de config>:/etc/odoo -v <ruta de modulos>:/mnt/extra-addons -p 8069:8069 --name odoo --link db:db -t odoo:12`
