# RabbitMQ

<b>RabbitMQ</b> is a message broker: it accepts and forwards messages. 

A <b>message broker</b> (also known as an integration broker or interface engine) is an intermediary computer program module that translates a message from the formal messaging protocol of the sender to the formal messaging protocol of the receiver.

![Message-broker](https://miro.medium.com/max/1302/0*p05ch77ERQOpj2GN.png)

You can think about <b>RabbitMQ</b> as a post office: when you put the mail that you want posting in a post box, you can be sure that Mr. or Ms. Mailperson will eventually deliver the mail to your recipient. In this analogy, RabbitMQ is a post box, a post office and a postman. 

<hr>

<b>Producing</b> means nothing more than sending. A program that sends messages is a producer :

![Producer](https://www.rabbitmq.com/img/tutorials/producer.png)

A <b>queue</b> is the name for a post box which lives inside RabbitMQ. Although messages flow through RabbitMQ and your applications, they can only be stored inside aqueue. A queue is only bound by the host's memory &disk limits, it's essentially a large message buffer. Many producers can send messages that go to one queue, and many consumers can try to receive data from onequeue. This is how we represent a queue:

![Queue](https://www.rabbitmq.com/img/tutorials/queue.png)

Consuming has a similar meaning to receiving. A consumer is a program that mostly waits to receive messages:

![Consumer](https://www.rabbitmq.com/img/tutorials/consumer.png)

Note that the producer, consumer, and broker do not have to reside on the same host; indeed in most applications they don't. An application can be both a producer and consumer, too. 

`"Hello World"`