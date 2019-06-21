# Simple Test with Go

RabbitMQ must be running in the Docker container before testing.

First, install amqp using go get:

```
go get github.com/streadway/amqp
```

Then build the send and receive apps:

```
go build receive.go

go build send.go
```

The send and receive Go code comes from the [Hello World - Getting Started](https://www.rabbitmq.com/tutorials/tutorial-one-go.html) section of the documentation on the RabbitMQ website.  Visit if you'd like a comprehensive explanation of what the code is doing.

Execute the receive app.  It will watch for messages arriving in the queue:

```
./receive
```

Then, in a separate terminal, execute the send app to send a message:

```
./send
```

Each time you execute the send app, you should see an acknowledgment from the receive app.

When you've finishing testing, [Ctrl-C] will terminate the receive app.
