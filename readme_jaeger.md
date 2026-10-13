# check yaml syntax right or wrong
docker compose -f docker-compose-jaeger.yaml config

docker compose -f docker-compose-jaeger.yaml up -d

# check running conta[text](docker-compose.yml)iners
docker compose -f docker-compose-jaeger.yaml ps

# first open fake-service UI and request generate - chrome
http://localhost:9999/ui

# click GO 2 or 3 times

# Jaeger
http://localhost:16686

# to stop everything later
docker compose -f docker-compose-jaeger.yaml down