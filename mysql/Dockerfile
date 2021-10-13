FROM guacamole/guacamole as temp_image_1
RUN echo "CREATE DATABASE IF NOT EXISTS guacamole;" > /initdb.sql
RUN echo "USE guacamole;" >> /initdb.sql
RUN /opt/guacamole/bin/initdb.sh --mysql >> /initdb.sql

FROM mysql as mysql_db
COPY --from=temp_image_1 /initdb.sql /docker-entrypoint-initdb.d/initdb.sql
