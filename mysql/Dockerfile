FROM mysql:5.7

RUN apt-get update && apt-get install -y openssl procps
COPY ./certs/server_certs/ca.pem /etc/mysql/ssl/ca.pem
COPY ./certs/server_certs/server-cert.pem /etc/mysql/ssl/server-cert.pem
COPY ./certs/server_certs/server-key.pem /etc/mysql/ssl/server-key.pem
COPY ./conf/ssl.cnf /etc/mysql/mysql.conf.d/ssl.cnf

RUN chown -R mysql: /etc/mysql
