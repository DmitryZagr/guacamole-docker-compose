# guacamole with keycloak authentication docker-compose

## prepare

```bash
$ git clone https://github.com/DmitryZagr/guacamole-docker-compose.git
$ cd guacamole-docker-compose
$ cd init 
$ docker run --rm guacamole/guacamole:0.9.14 /opt/guacamole/bin/initdb.sh --postgres > initdb.sql
$ cd ..
```

## run

```bash
docker-compose up -d
```

## configure keycloak

+ Go to `http://DOCKER_HOST:8081/auth`
+ Log into admin console with `admin` `admin` credentials
+ Add new keycloak client:
  + Specify the client id - `guacamole`
  + Turn on Implicit Flow Enabled toggle button
  + Specify Valid Redirect URIs - `*`

## using guacamole

Then go to `http://DOCKER_HOST:8080/guacamole/`
Log in as any user specified in keycloak.
