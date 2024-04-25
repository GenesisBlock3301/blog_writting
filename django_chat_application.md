# Making Chat Application With Django Channel

### What is WebSocket?
WebSocket is a com

## What is Django channel?
Django channel is the extension of Django web framework that enables handling real-time functionality, like WebSocket,
Asynchronous code and background task. It allows to Django application handle more than just traditional HTTP requests.

How does Django Channel works:

### Asynchronous Support:
Asynchronous support often referred to as support asynchronous programming, this is a one kind of programming paradigm 
that allows task to be executed concurrently without the need for explicit parallel threads or processes.
In web development & server side programming, asynchronous support is crucial to handle concurrent connection efficiently.

- #### Concurrency VS Parallelism:
    In `Concurrency` multiple task occurred at the same time, even if only one task is being actively executed at any given 
    moment. It doesn't necessarily involve parallel execution.
    `Concurrency` happen in single thread.
    
    In `Parallelism` involves simultaneously execution of multiple tasks. It uses multiple core or threads
    that's it works parallely.
- #### Asynchronous Programming:
    In `Asynchronous Programming` task initiated and executed independently, no program wait for another one.
    It is useful for handling I/O bound operation such as reading from or writing from database, making API call or reading 
    file. During these operation the program can continue to perform other task instead of blocking and waiting the I/O 
    operation to complete.

### Consumer:
Consumer it's like django but views, but in channel that defines how to handle different types of connections or events.
Consumers are responsible for processing WebSocket messages and manages asynchronous task.

### Routing:
Routing maps the incoming request to the proper consumer, same as django urls.

### Channels Layer:
It adds a layer on django application that allows it to communicate with other part of system using django channels.
A channel layer is a kind of communication system. It allows multiple consumer instance to talk each other and with other
part of django.
Channel layer has a couple of abstraction:
- A channel is kind of mailbox where message can be sent to. Each channel has name, Anyone who has the name of channel
can send & read the message of this channel.
- A group
### Channels Server:
By default, Django use WSGI servers, Django Channel use ASGI server(Asynchronous Server Gateway Interface). This ASGI 
server can handle both traditional HTTP request and Asynchronous Websocket.

### Background Task:
Django channel can handle background task of an application.

### Django Channel VS Django Celery:

Both Channel & Celery support asynchronous task execution, but they are designed to different purpose
- #### Django Channel:
  - Mainly focused on handling real-time communication, including support for WebSockets.
  - Channel can be used for managing long-lived connections and handling real-time updates in your Django application.

- #### Django Celery:
    
   - This is distributed task queue system designed for handling background tasks and asynchronous processing.
   - Enables you to offload time-consuming or resource-intensive tasks to be executed asynchronously in the background.
   - Well-suited for tasks like sending emails, processing large datasets, running periodic jobs, and other background 
  processing needs.