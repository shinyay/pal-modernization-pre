# Movie Fun!

Smoke Tests require server running on port 8080 by default.

## Build WAR ignoring Smoke Tests

```
$ mvn clean package -DskipTests -Dmaven.test.skip=true
```

## Run Smoke Tests against specific URL

```
$ MOVIE_FUN_URL=http://moviefun.example.com mvn test
```

## Setup Database

```
$ docker-compose up -d
$ mysql -h127.0.0.1 -uroot -pmysql -e 'DROP DATABASE IF EXISTS movies; CREATE DATABASE movies;'
$ mysql -h127.0.0.1 -uroot -pmysql movies < ./db/schema.ddl
```

## Setyo Minio

- [Minio Dashboard: http://localhost:9000](http://localhost:9000)

  - AccessKey: access_key
  - SecretKey: access_secret
  - Bucket: movie-fun-course (Create on Dashboard)
