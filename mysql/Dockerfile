FROM percona:5.7

RUN rm /etc/mysql/percona-server.conf.d/*

COPY mysqld.cnf /etc/mysql/percona-server.conf.d/mysqld.cnf

ENV MYSQL_ALLOW_EMPTY_PASSWORD yes
ENV MYSQL_ROOT_PASSWORD root
ENV MYSQL_USER symfony
ENV MYSQL_PASSWORD symfony
