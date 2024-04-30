FROM mysql:8.0.33 
LABEL "Project" = "Vprofile"
LABEL "Author" = "Necs"

ENV MYSQL_ROOT_PASSWOR ="vprodbpass"
ENV MYSQL_DATABASE ="accounts"
ADD db_backup.sql /docker-entrypoint-initdb.d/db_backup.sql
EXPOSE 3306
