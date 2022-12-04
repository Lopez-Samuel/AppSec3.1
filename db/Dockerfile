FROM mysql:latest

RUN mkdir /data
COPY ./products.csv /data/products.csv
COPY ./users.csv /data/users.csv
COPY ./seeding/db-seed.sql /docker-entrypoint-initdb.d/db-seed.sql

ENTRYPOINT ["/entrypoint.sh"]
CMD ["mysqld", "--secure-file-priv=/data"]
#CMD ["--secure-file-priv=/"]