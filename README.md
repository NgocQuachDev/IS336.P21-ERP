# IS336.P21 - ERP
Odoo modules development

# Guides
## Set Up a Custom Module with Docker
... To be continue

## Set Up Odoo with Docker
After download and open Docker Desktop, use terminal:

```sh
docker --version
```

Pull latest images
- Odoo: 
```sh
docker pull odoo:latest
```

- Postgres: 
```sh
docker pull postgres:latest
```
Local Directory Set Up
- Create a folder

```sh
mkdir odoo18
```

- Create a postgres password file ("0123456789abc" = any password)
```sh
echo "0123456789abc" > odoo_pg_pass
```

- Create a <b>docker-compose.yaml</b>

- Build the composer
```sh
docker compose up -d
```
- Check the container logs (optional)
```sh
docker compose logs -f
```
- Check the connection
```sh
# Correct: HTTP/1.1 200 OK
curl -Is http://localhost:8069
```
- Open browser to connect: <b>localhost:8069</b>

- To shutdown container:
```sh
docker compose down
```
