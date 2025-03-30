FROM postgres:13

ENV POSTGRES_USER=user
ENV POSTGRES_PASSWORD=user
ENV POSTGRES_DB=wake_db

EXPOSE 5432

COPY ./data/wake_db.sql /docker-entrypoint-initdb.d/wake_db.sql
