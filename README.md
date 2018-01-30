# guacamole-docker-compose

## prepare

```bash
$ git clone https://github.com/DmitryZagr/guacamole-docker-compose.git
$ cd guacamole-docker-compose
$ cd init 
$ docker run --rm guacamole/guacamole:0.9.13-incubating /opt/guacamole/bin/initdb.sh --postgres > initdb.sql
$ cd ..
```

## run

```bash
docker-compose up -d
```

Then go to `http://DOCKER_HOST:8080/guacamole/`

Log in as user: `guacadmin` and password: `guacadmin`.
