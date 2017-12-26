# Docker Compose Dengan PHP

## Langkah pertama membuat Dockerfile

```
FROM php:7.0-apache
COPY src/ /var/www/html/
EXPOSE 80
```

## Langkah kedua membuat docker-compose.yml

```
version: '3'
services:
  web:
    build: .
    ports:
     - "8000:80"
```

## Langkah ketiga lakukan build dengan menggunakan perintah
```
docker-compose up 
atau
docker-compose build kemudian jalankan perintah docker-compose up
```
Lakukan pengujian dengan membuka pada browser localhost:8080/
