# Authentication

## Securing Passwords with Bcrypt Hashing Function

- PROBLEMS WITH CRYPTOGRAPHIC HASH ALGORITHM:

**Brute Force attack:** Hashes can't be reversed, so instead of reversing the hash of the password, an attacker can simply keep trying different inputs until he does not find the right now that generates the same hash value, called brute force attack.

**Hash Collision attack:** Hash functions have infinite input length and a predefined output length, so there is inevitably going to be the possibility of two different inputs that produce the same output hash.

**BCrypt, IT's SLOW AND STRONG AS HELL:**
To overcome such issues, we need algorithms which can make the brute force attacks slower and minimize the impact. Such algorithms are PBKDF2 and BCrypt, both of these algorithms use a technique called Key Stretching.

## Basic access authentication

In the context of an HTTP transaction, basic access authentication is a method for an HTTP user agent (e.g. a web browser) to provide a user name and password when making a request. In basic HTTP authentication, a request contains a header field in the form of Authorization: Basic credentials, where credentials is the Base64 encoding of ID and password joined by a single colon : .

- Features:
HTTP Basic authentication (BA) implementation is the simplest technique for enforcing access controls to web resources because it does not require cookies, session identifiers, or login pages; rather, HTTP Basic authentication uses standard fields in the HTTP header.

- Protocol:

1. Server side:
When the server wants the user agent to authenticate itself towards the server after receiving an unauthenticated request, it must send a response with a HTTP 401 Unauthorized status line and a WWW-Authenticate header field.

2. Client side:
When the user agent wants to send authentication credentials to the server, it may use the Authorization header field.

## Introduction to Authentication

- Authentication: is the process of verifying that an individual, entity or website is whom it claims to be. Authentication in the context of web applications is commonly performed by submitting a username or ID and one or more items of private information that only a given user should know.

- Session Management: is a process by which a server maintains the state of an entity interacting with it. This is required for a server to remember how to react to subsequent requests throughout a transaction. Sessions are maintained on the server by a session identifier which can be passed back and forward between the client and server when transmitting and receiving requests. Sessions should be unique per user and computationally very difficult to predict. The Session Management Cheat Sheet contains further guidance on the best practices in this area.

- Change Password Feature:

1. User is authenticated with active session.
2. Current password verification. This is to ensure that it's the legitimate user who is changing the password. The abuse case is this: a legitimate user is using public computer to login. This user forgets to logout. Then another user is using this public computer. If we don't verify current password, this another user able to change the password.

## node.bcrypt.js

A library to help you hash passwords.
