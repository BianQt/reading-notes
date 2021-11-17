# Event Driven Architecture

## Review, Research, and Discussion

* What’s the difference between a FIFO and a standard queue?
    - Standard queues provide at-least-once delivery, which means that each message is delivered at least once. FIFO queues provide exactly-once processing, which means that each message is delivered once and remains available until a consumer processes it and deletes it.

* How can the server be assured a message was properly received?
   - Using queues and save them in database.
* What classic design pattern is best represented by event driven programming?
   - It is the most basic pattern describing event-centric communication facilitated by the Event Store. It embraces the triggering function of Events.
* How do you test an event driven system?
   - n an event-driven system, Payment Service’s contract is different. Rather than HTTP messages, it operates on events. In this case, the service “promises” to process a payment and emit a Payment Successful event on the Payments topic, when there is a new order placed on the Orders topic.


## Vocabulary Terms

* **FIFO Queue** : A FIFO queue is a queue that operates on a first-in, first-out (FIFO) principle. This means that the request (like a customer in a store or a print job sent to a printer) is processed in the order in which it arrives.

* **Pub/Sub** : Stands for Publisher/Subscriber, allows services to communicate asynchronously, with latencies on the order of 100 milliseconds.

## Preview
* Which 3 things had you heard about previously and now have better clarity on?
  - AWS
  - Socket io

* Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
  - Events
  - Authentication - Testing

* What are you most excited about trying to implement or see how it works?
  - AWS
  - Authentication
  - SQL Databases

## Preparation Materials

### AWS SNS and SQS
#### SNS
Amazon Simple Notification Service (Amazon SNS) is a web service that makes it easy to set up, operate, and send notifications from the cloud. It provides developers with a highly scalable, flexible, and cost-effective capability to publish messages from an application and immediately deliver them to subscribers or other applications. It is designed to make web-scale computing easier for developers. Amazon SNS follows the “publish-subscribe” (pub-sub) messaging paradigm, with notifications being delivered to clients using a “push” mechanism that eliminates the need to periodically check or “poll” for new information and updates. With simple APIs requiring minimal up-front development effort, no maintenance or management overhead and pay-as-you-go pricing, Amazon SNS gives developers an easy mechanism to incorporate a powerful notification system with their applications.
#### SQS
Amazon Simple Queue Service (SQS) and Amazon SNS are both messaging services within AWS, which provide different benefits for developers. Amazon SNS allows applications to send time-critical messages to multiple subscribers through a “push” mechanism, eliminating the need to periodically check or “poll” for updates. Amazon SQS is a message queue service used by distributed applications to exchange messages through a polling model, and can be used to decouple sending and receiving components. Amazon SQS provides flexibility for distributed components of applications to send and receive messages without requiring each component to be concurrently available.

A common pattern is to use SNS to publish messages to Amazon SQS queues to reliably send messages to one or many system components asynchronously.