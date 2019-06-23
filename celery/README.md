# Using Celery with RabbitMQ

This assumes you've already set up RabbitMQ in a Docker container, and it's running.

Info comes from [here](http://docs.celeryproject.org/en/latest/getting-started/first-steps-with-celery.html).

## Description

Celery is a task queue for Python.

## Setup

Since Celery is a standard Python package, you can install it with Pip:

```
sudo pip3 install celery
```

## Testing

Run the `tasks.py` script as follows:

```
celery -A tasks worker --loglevel=info
```

A worker instance will start up, and wait for tasks.

In a separate terminal, execute `calltask.py`:

```
./calltask.py
```

You'll see a confirmation in the worker window, similar to this:

```
[2019-06-22 22:22:57,330: INFO/MainProcess] Received task: tasks.add[e9b2ab91-273e-4c57-889f-ca467a601cf9]  
[2019-06-22 22:22:57,330: INFO/ForkPoolWorker-2] Task tasks.add[e9b2ab91-273e-4c57-889f-ca467a601cf9] succeeded in 6.74980110488832e-05s: 8
```
