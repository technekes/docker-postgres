# Docker Postgres

Docker image forked from the following git repo:

appropriate/docker-postgis


# Description

The postgis image provides a Docker container running Postgres 9 with PostGIS 2.1 installed. This image is based on the official postgres image and provides variants for each version of Postgres 9 supported by the base image (9.0-9.4).

This image ensures that the default database created by the parent postgres image will have the postgis and postgis_topology extensions installed. Unless -e POSTGRES_DB is passed to the container at startup time, this database will be named after the admin user (either postgres or the user specified with -e POSTGRES_USER). For Postgres 9.1+, the fuzzystrmatch and postgis_tiger_geocoder extensions are also installed.

If you would prefer to use the older template database mechanism for enabling PostGIS, the image also provides a PostGIS-enabled template database called template_postgis.
