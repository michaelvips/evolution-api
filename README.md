
How to build a new image with logs
docker build -t evolution/api:local . > build-dockerfile.log 2>&1

How to build a new image using docker compose with Dockerfile with logs
docker-compose -f docker-compose.dev.yaml up -d --build > build-compose.log 2>&1

Rename the image
docker tag 0d120b6ccaae michaelvips/evolution-api:v2.2.0-develop

Enviando imagem docker hub - antes certifique-se de que o repo ja exista
1 login = docker login
2 enviar = docker push michaelvips/evolution-api:v2.2.0-develop