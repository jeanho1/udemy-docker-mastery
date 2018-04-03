# Assignment: Named Volumes

> Goal: Database Upgrades with Named Volumes

- Database upgrade with containers
- Create a `postgres` container with named volume psql-data using version `9.6.1`
- Use Docker Hub to learn VOLUME path and versions needed to run it
	- `docker container run -d --name psql -v psql:/var/lib/postgresql/data postgres:9.6.1`
- Check logs, stop container
	- `docker container logs -f psql`
	- `docker container stop psql`
- Create a new postgres container with same named volume using `9.6.2`
	- `docker container run -d --name psql2 -v psql:/var/lib/postgresql/data postgres:9.6.2`
	- `docker volume ls` - check if volume=`psql`