# Docker Compose + Jaeger

## Check YAML syntax

docker compose -f docker-compose-jaeger.yaml config

If there is no error, start all containers:

docker compose -f docker-compose-jaeger.yaml up -d

## Check running containers

docker compose -f docker-compose-jaeger.yaml ps

## Open Fake Service UI

Open in browser:

http://localhost:9999/ui

Click Go 2 - 3 times to generate requests and traces.

## Open Jaeger UI

Open in browser:

http://localhost:16686

Select Product Page, then click Find Tracesto view the service trace.

## Stop the lab

docker compose -f docker-compose-jaeger.yaml down