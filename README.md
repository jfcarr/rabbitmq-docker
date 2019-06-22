# Running and Testing RabbitMQ In a Docker Container

Retrieve RabbitMQ docker container:

```
sudo docker pull rabbitmq
```

Startup for RabbitMQ docker container:

```
sudo docker run -d --hostname my-rabbit --name some-rabbit -p 5672:5672 rabbitmq:3
```

> **The port mapping (5672:5672) is important. It's not included in the instructions on Docker Hub, but it's required for the Python send/receive scripts to work.**

After setup, you can subsequently stop and restart the RabbitMQ instance with the following commands:

```
sudo docker stop some-rabbit

sudo docker start some-rabbit
```