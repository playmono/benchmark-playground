SERVICE_NAME ?= backoffice_kotlin
DOCKER_COMPOSE = docker-compose -p $(SERVICE_NAME) -f docker/docker-compose.yaml --env-file .env

build:
	@test -s .env || cp .env.dist .env
	$(DOCKER_COMPOSE) build --pull

stop:
	$(DOCKER_COMPOSE) down

start:
	$(DOCKER_COMPOSE) up -d

ssh:
	$(DOCKER_COMPOSE) exec container /bin/sh