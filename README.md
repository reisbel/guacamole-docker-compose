# docker-compose for Apache Guacamole

Run [Apache Guacamole](https://guacamole.apache.org/) with docker containers using docker-compose, based on the [Official Documentation](https://guacamole.apache.org/doc/gug/guacamole-docker.html)

## Use
Edit .env, changing the username and password for postgres database.
```cfg
//.env
POSTGRES_USER=new_postgres_username
POSTGRES_PASSWORD=new_secure_postgres_password
```
## Start
First you should get the seed file for postgres.
```bash
docker-compose up init-guacamole-db
```
Then you can start everything.

## Steps process

Clone repository
```bash
git clone https://github.com/reisbel/guacamole-docker-compose.git && cd guacamole-docker-compose
```

Make changes to .env
```bash
vim .env 
```

Seed postgres database
```bash
docker-compose up init-guacamole-db
```

Start everything
```bash
docker-compose up -d
```

Guacamole is now listening on port 8080

default username: guacadmin
default password: guacadmin

Be sure to change the default password.


## Guacamole Manual
https://guacamole.apache.org/doc/gug/


## License

MIT - See [LICENSE](LICENSE) for more information.