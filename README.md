# TODO-SYNC-BACKEND

This project is the backend of an architecture of an app that syncs data between multiple apps by publishing to a queue.

It's an experiment to check wether the architecture is feasible.

The service will be responsible for reading data from the queue, saving it to the database and then publishing the updates to the client apps

## Running the project (In construction)

After downloading this repo, you can do the following:

1. Start the queue using the docker-compose.yml file:

        docker compose up

This will start up the queue and the database with default configs

2. Copy the file ``.env.example`` and rename it to ``.env`` and put the same configs you set up on the docker-compose.yml file

3. Execute

        go run main.go

*** 
## Info - The configs below refer to first version

Until now this was directly taken from the rabbitmq docs:

> https://www.rabbitmq.com/tutorials/tutorial-one-go.html

Start the receiver:

    go run receive.go

Start the sender:

    go run send.go