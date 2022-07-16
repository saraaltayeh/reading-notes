# AWS: API, Dynamo and Lambda

- What is Amazon API Gateway?

Amazon API Gateway is a managed service that allows developers to define the HTTP endpoints of a REST API or a WebSocket API and connect those endpoints with the corresponding backend business logic. It also handles authentication, access control, monitoring, and tracing of API requests.

- Why is API Gateway an essential part of the Serverless ecosystem?

Within the Serverless ecosystem, API Gateway is the piece that ties together Serverless functions and API definitions. Being able to trigger the execution of a Serverless function directly in response to an HTTP request is the key reason why API Gateway is so valuable in Serverless setups: it enables a truly serverless architecture for web applications. When using API Gateway together with other AWS services, it’s possible to build a fully functional customer-facing web application without maintaining a single server yourself.

- How does API Gateway integrate with other AWS services?

AWS Lambda: run Lambda functions to generate HTTP API responses.
AWS SNS: publish SNS notifications when an HTTP API endpoint is accessed.
Amazon Cognito: provide authentication and authorization for your HTTP APIs.

- What are the some benefits of using Amazon API Gateway?

1. Efficient API development
2. Performance at any scale
3. Cost savings at scale
4. Easy monitoring
5. Flexible security controls
6. RESTful API options

## API Types

- RESTful APIs
Build RESTful APIs optimized for serverless workloads and HTTP backends using HTTP APIs. HTTP APIs are the best choice for building APIs that only require API proxy functionality. If your APIs require API proxy functionality and API management features in a single solution, API Gateway also offers REST APIs.

- WEBSOCKET APIs
Build real-time two-way communication applications, such as chat apps and streaming dashboards, with WebSocket APIs. API Gateway maintains a persistent connection to handle message transfer between your backend service and your clients.

## AWS DynamoDB Guide

- What is DynamoDB?
DynamoDB is a hosted NoSQL database offered by Amazon Web Services (AWS). It offers:

reliable performance even as it scales;
a managed experience, so you won't be SSH-ing into servers to upgrade the crypto libraries;
a small, simple API allowing for simple key-value access as well as more advanced query patterns.

## How it works (Amazon DynamoDB)

Amazon DynamoDB is a fully managed, serverless, key-value NoSQL database designed to run high-performance applications at any scale. DynamoDB offers built-in security, continuous backups, automated multi-Region replication, in-memory caching, and data export tools.

![img](https://d1.awsstatic.com/product-page-diagram_Amazon-DynamoDBa%402x.1f8b0cf0312dda72ce9433d94f9c2a1b92684381.png)

## Dynamoose

Dynamoose: is a modeling tool for Amazon's DynamoDB. Dynamoose is heavily inspired by Mongoose, which means if you are coming from Mongoose the syntax will be very familar.

- Key Features:

1. Type safety
2. High level API
3. Easy to use syntax
4. Ability to transform data before saving or retrieving documents
5. Strict data modeling (validation, required attributes, and more)
6. Support for DynamoDB Transactions
7. Powerful Conditional/Filtering Support
8. Callback & Promise support
