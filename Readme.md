# Introduction

# Tech stack

1. GO
2. Micro-service
3. Kafka
4. MongoDb

# Requirements

## Phase 1

Functional : 

- Users should be able to register through the client application (Mobile app/web app).
- Users should be able to delete existing account.
- Users should be able to discover other users.
- Users should be able to exchange text messages with other users.
- Users should be able to create groups.
- Users should be able to view history of chats.

Non-functional :

- Unit and integration test. Maintain coverage above 80% +. 
- Performance tests with respect to TCP connections per server.
- Maximum data per Database that can be supported. 
- Security testing w.r.t to end-to-end encryption.

# Ramp-up guidelines

## Week 1

- We will be using GO as the backend language. Please go through following courses to learn GO:
  - Getting started with GO [https://app.pluralsight.com/library/courses/getting-started-with-go/table-of-contents]

- Go through this document thoroughly for creating good REST APIs -
  - REST API guidelines [https://github.com/microsoft/api-guidelines/blob/vNext/Guidelines.md]

- Testing GO applications
  - Go create test applications [https://app.pluralsight.com/library/courses/go-create-test-applications/table-of-contents]

## Week 2

- How TCP works?
  
- Kafka

- https://www.confluent.io/blog/how-choose-number-topics-partitions-kafka-cluster/

## Week 3

- MongoDb (specifically with GO)

- Micro-services tooling - [https://github.com/mfornos/awesome-microservices#go]


# Initial Flow

## 2 users want to share test message
- Each user has a device/browser with TCP connection to the server. 
- Client 1 (with IP1) sends message. The message goes to Server.
- Message has destination I/P or user ID of Client 2.
- Server finds the TCP connection object of client 2.
- Server sends the message over that TCP connection to client 2.
- Save transaction details in DB.
- Client 2 will get a notification.
  - Client is up and having live connection, then the message should be pushed immediately
  - CLient is not having live connection, add the message to queue

    1  ->  [t1, U2, TS], [t2, U5, TS], [t3, U4, TS] 
    2  ->
    3  ->
    4  ->
    5  ->

- Is it a good idea to have 1 Kafka topic per client? (per message?)

# Services

## User registration service

## Message service

## Audit (Log) service

## MongoDb