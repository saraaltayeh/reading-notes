# AWS: Events

## AWS — Difference between SQS and SNS

- SNS (Simple Notification Service):

Amazon SNS is a fast, flexible, fully managed push notification service that lets you send individual messages or to bulk messages to large numbers of recipients.
Amazon SNS is a fast, flexible, fully managed push notification service that lets you send individual messages or to bulk messages to large numbers of recipients.
SNS supports several end points such as email, sms, http end point and SQS. If you want unknown number and type of subscribers to receive messages, you need SNS.

- SQS (Simple Queue Service)

Amazon SQS is a fully managed message queuing service that enables you to decouple and scale microservices, distributed systems, and serverless applications.
SQS is distributed queuing system. Messages are not pushed to receivers. Receivers have to poll SQS to receive messages. Messages can be stored in SQS for short duration of time (max 14 days).
Messages can’t be received by multiple receivers at the same time. Any one receiver can receive a message, process and delete it.

- Use Cases:

Choose SNS if:

1. You would like to be able to publish and consume batches of messages.
2. You would like to allow same message to be processed in multiple ways.
3. Multiple subscribers are needed.

Choose SQS if:

1. You need a simple queue with no particular additional requirements.
2. Decoupling two applications and allowing parallel asynchronous processing.
3. Only one subscriber is needed.
