Install docker 

```
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh ./get-docker.sh
```

Replace <KEY> and <DB_PASSWORD> in .env and .db.env

Enable docker to be run as non-root user 

```
sudo usermod -aG docker ${USER}
```

Re-login, and then start container 

```
docker compose -f docker-compose.yml up -d --pull=always
```

Check status of installation

```
docker compose -f docker-compose.yml logs -f
```
