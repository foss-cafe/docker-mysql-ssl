# MySQL Docker Image with TLS support

### Base Image
 - MySQL 5.7

## TLS certificates
You can find certs in  `mysql/certs` Dir.

 - `server-cert.pem` : MySQL server certificate
 - `server-key.pem` : MySQL server key
 - `ca-key.pem` : MySQL CA Key
 - `ca.pem` : MySQL CA Certificate
 - `client-cert.pem` : Client certificate (signed by CA)
 - `client-key.pem` : Client key

## Connect with MySQL Client

Run the container:
```
docker-compose up -d
```

Connect to the server:
```
mysql -u root -p -h 127.0.0.1 --ssl-ca=mysql/certs/client_cert/ca.pem --ssl-cert=mysql/certs/client_cert/client-cert.pem --ssl-key=mysql/certs/client_cert/client-key.pem
```
