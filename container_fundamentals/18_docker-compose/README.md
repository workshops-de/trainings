# Docker Compose

In this course we will install a minimal Prometheus stack via Docker Compose.

## Inspect the file `prometheus.yml`

## Inspect the Docker Compose file called `docker-compose.yml`

## Start all containers

```bash
docker-compose up -d
# Verify everything is working
docker ps
# Check the exposed metrics of CAdvisor
curl localhost:8080/metrics
```

## Visit Grafana in your Browser

Use webpreview to access grafana. Remember to use port 8081.
Default credentials for grafana are:
User: admin
Password: admin

## Create a Datasource

Create a Datasource of type `Prometheus` and the URL `http://prometheus:9090`

## Import a Dashboard

Import the Dashboard with id `193`. Set the Datasource to the previously generated.

## Cleanup

```bash
docker-compose down
```
