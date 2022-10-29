FROM mysql:5.7.25
LABEL "Project"="Vprofile"
LABEL "AUthor"="Kusam"

ADD db_backup.sql docker-entrypoint-initdb.d/db_backup.sql
ENV MYSQL_ROOT_PASSWORD="vprodbpass"
ENV MYSQL_DATABASE="accounts"