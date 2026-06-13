FROM mysql:8.0

# Set environment variables (you can override in docker run / compose)
ENV MYSQL_ROOT_PASSWORD=rootpass
ENV MYSQL_DATABASE=accounts
ENV MYSQL_USER=admin
ENV MYSQL_PASSWORD=admin123

# Copy initialization SQL (vprofile schema)
COPY db_backup.sql /docker-entrypoint-initdb.d/

EXPOSE 3306