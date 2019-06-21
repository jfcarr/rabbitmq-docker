# Simple Test with Python

RabbitMQ must be running in the Docker container before testing.

First, install the Pika library using pip:

```
sudo pip3 install pika
```

The send and receive scripts come from the [Hello World - Getting Started](https://www.rabbitmq.com/tutorials/tutorial-one-python.html) section of the documentation on the RabbitMQ website.  Visit if you'd like a comprehensive explanation of what the scripts are doing.

Execute the receive app.  It will watch for messages arriving in the queue:

```
./receive.py
```

Then, in a separate terminal, execute the send app to send a message:

```
./send.py
```

Each time you execute the send app, you should see an acknowledgment from the receive app.

When you've finishing testing, [Ctrl-C] will terminate the receive app.
