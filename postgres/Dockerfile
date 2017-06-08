FROM postgres:9.6.3-alpine

VOLUME /var/lib/postgresql/data

ADD seed.sql /docker-entrypoint-initdb.d/

EXPOSE 5432
