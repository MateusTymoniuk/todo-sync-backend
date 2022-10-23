# TODO-SYNC-BACKEND

This project is the backend of an architecture of an app that syncs data between multiple apps by publishing to a queue.

It's an experiment to check wether the architecture is feasible.

The service will be responsible for reading data from the queue, saving it to the database and then publishing the updates to the client apps

## Info

Until now this was directly taken from the rabbitmq docs:

> https://www.rabbitmq.com/tutorials/tutorial-one-go.html

## Running the project

After downloading this repo, you can do the following:

1. Start the queue using the docker-compose.yml file:

    `docker compose up`

2. Start the receiver:

    `go run receive.go`

3. Start the sender:

    `go run send.go`