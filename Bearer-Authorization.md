# Bearer Authorization

## JWTs

is a very modern, simple and secure approach which extends for Json Web Tokens. Json Web Tokens are a stateless solution for authentication. So there is no need to store any session state on the server, which of course is perfect for restful APIs. Restful APIs should always be stateless, and the most widely used alternative to authentication with JWTs is to just store the user's log-in state on the server using sessions. But then of course does not follow the principle that says that restful APIs should be stateless and that's why solutions like JWT became popular and effective.

The token is created using a secret string that is stored on a server. Next, the server then sends that JWT back to the client which will store it either in a cookie or in local storage.

![jwt img](./images/jwt.png)

- **What is JSON Web Token?**

JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. This information can be verified and trusted because it is digitally signed. JWTs can be signed using a secret (with the HMAC algorithm) or a public/private key pair using RSA or ECDSA.

- **What is the JSON Web Token structure?**

In its compact form, JSON Web Tokens consist of three parts separated by dots (.), which are:

1. Header
2. Payload
3. Signature

Therefore, a JWT typically looks like the following:
xxxxx.yyyyy.zzzzz

- **Why should we use JSON Web Tokens?**

As JSON is less verbose than XML, when it is encoded its size is also smaller, making JWT more compact than SAML. This makes JWT a good choice to be passed in HTML and HTTP environments.

Security-wise, SWT can only be symmetrically signed by a shared secret using the HMAC algorithm. However, JWT and SAML tokens can use a public/private key pair in the form of a X.509 certificate for signing. Signing XML with XML Digital Signature without introducing obscure security holes is very difficult when compared to the simplicity of signing JSON.
