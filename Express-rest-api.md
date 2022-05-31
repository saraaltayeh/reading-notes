# Express REST API

## Classes

Classes are in fact "special functions", and the class syntax has two components: class expressions and class declarations.

- Class declarations
One way to define a class is using a class declaration. To declare a class, you use the class keyword with the name of the class.

- Class expressions:
A class expression is another way to define a class. Class expressions can be named or unnamed. The name given to a named class expression is local to the class's body.

## Routing

You define routing using methods of the Express app object that correspond to HTTP methods; for example, app.get() to handle GET requests and app.post to handle POST requests.

### create an application that has some routes and a few features

- Basic Routes: Home, About
- Route Middleware to log requests to the console
- Route with Parameters
- Route Middleware for Parameters to validate specific parameters
- Login routes Doing a GET and POST on /login
- Validates a parameter passed to a certain route

### Application Structure

- package.json  // set up our node packages
- server.js     // set up our app and build routes
