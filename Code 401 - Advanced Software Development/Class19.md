# AWS: Events
>
## Review, Research, and Discussion

1. Describe the similarities between AWS API Gateway + Lambda functions and an ExpressJS Server?

        Amazon API Gateway is a fully managed service that makes it easy for developers to create, publish, maintain, monitor, and secure APIs at any scale

2. List the AWS Database offerings and talk about the pros and cons of each?

        Relational: It's good in orgnize the DB in tables and make relations between tables
        NoSQL: It's fast in reading the data

3. What’s the difference between a FIFO and a standard queue?

        Standard queues guarantee that a message is delivered at least once and duplicates can be introduced into the queue FIFO queues ensure a message is delivered exactly once and remains available until a consumer processes and deletes it

4. How can the server be assured a message was properly received?

        by hit an event after receiving a message

## Document the following Vocabulary Terms

* **Serverless API:**

  * using API Gateway you can create RESTful APIs that enable real-time two-way communication applications, API Gateway supports containerzied and serverless workloads as well as web applications.

* **Triggers:**

  * an AWS Lambda resource or resource in another service that you configure to invoke your function in response to lifecycle events, external requests or on a schedule, a function can have multiple triggers.

* **Dynamo vs Mongo:**

  * Mongo can be deployed anywhere, Dynamo is only available on AWS Mongo is JSON based document store, Dynamo is limited key-value store with JSON support Mongo is rich query language, Dynamo is key-value queries.

* **Dynamoose vs Mongoose:**

  * Dynamoose is a DynamoDB API structured like Mongoose, lets us provide a schema and perform CRUD operations against a DynamoDB table, installed via node and configured based on role.

## Preview

1. Which 3 things had you heard about previously and now have better clarity on? SQL, AUTH and API

2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo? AWS

3. What are you most excited about trying to implement or see how it works? AWS

## Preparation Materials

### AWS SQS vs SNS

**SNS (Simple Notification Service):**

    Amazon SNS is a fast, flexible, fully managed push notification service that lets you send individual messages or to bulk messages to large numbers of recipients. Amazon SNS makes it simple and cost effective to send push notifications to mobile device users, email recipients or even send messages to other distributed services. A distributed publish-subscribe system. Messages are pushed to subscribers as and when they are sent by publishers to SNS ,SNS supports several end points such as email, sms, http end point and SQS. If you want unknown number and type of subscribers to receive messages, you need SNS. With Amazon SNS, you can send push notifications to Apple, Google, Fire OS, and Windows devices , as well as to Android devices in China with Baidu Cloud Push. You can use SNS to send SMS messages to mobile device users in the US or to email recipients worldwide. SNS is a distributed publish-subscribe system. Messages are pushed to subscribers as and when they are sent by publishers to SNS.

**SQS (Simple Queue Service):**

    SQS is distributed queuing system. Messages are not pushed to receivers. Receivers have to poll SQS to receive messages. Messages can’t be received by multiple receivers at the same time. Any one receiver can receive a message, process and delete it. Other receivers do not receive the same message later. Polling inherently introduces some latency in message delivery in SQS unlike SNS where messages are immediately pushed to subscribers. SQS is mainly used to decouple applications or integrate applications. Messages can be stored in SQS for short duration of time (max 14 days). SNS distributes several copies of message to several subscribers. For example, lets say you want to replicate data generated by an application to several storage systems. You could use SNS and send this data to multiple subscribers, each replicating the messages it receives to different storage systems (s3, hard disk on your host, database, etc.).

## Resources

[SQS and SNS Basics](https://www.youtube.com/watch?v=UesxWuZMZqI)

[AWS SQS vs SNS](https://medium.com/awesome-cloud/aws-difference-between-sqs-and-sns-61a397bf76c5)
