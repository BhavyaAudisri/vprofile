FROM mysql:8.0
# Copy initialization SQL (vprofile schema)
COPY db_backup.sql /docker-entrypoint-initdb.d/

EXPOSE 3306