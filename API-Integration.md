# API Integration

## Dynamic API Server

An Express/Node.js based server designed to be a “model agnostic” REST API server, which can perform CRUD operations on any data model

## Obey a standard routing structure

- /api/v# where # is the version number of our API
- /model where ‘model’ is the name of the data model to operate on
- /id where ‘id’ is the id number of a specific entity in the data model
- Allow for Query String parameters for filtering
- This would GET every entry in our products data model where the category is ‘electronics’

Examples
GET Records (CRUD: READ)
GET MANY: [http://amazingapi.com/api/v1/products] or [http://amazingapi.com/api/v1.products?category=electronics]

```javascript
  {
    count: 300,
    previous: null,
    next: http://amazingapi.com/api/v1/products?page=2
    results: [
      { name: 'camera', ... },
      { name: 'phone', ... },
      { name: 'tv', ... },
      ...
    ]
  }
```

## Authentication Server / Module

An Express/Node.js based server using a custom “authentication” module that is designed to handle user registration and sign in using Basic, Bearer, or OAuth along with a custom “authorization” module that will grant/deny users access to the server based on their role or permissions level.

### Data Model

We will need to store user information into our system permanently. Use following fields/data types

### Users

username: Type: String, Required
password: Type: String, Required
email: Type: String
fullname: Type: String
role: Type: String, must be one of: admin, editor, writer, user
Application Structure (proposed)
NOTE: The majority of our work for this server will be done within the src/auth folder. The rest of the system should be generic express. Why? It’s our intention to be able to “lift” the auth folder and “drop” it into any other server (such as our API server) and be able to use authorization to “protect” those CRUD routes. This makes our entire auth system very modular. Think of index.js and server.js as nothing more than the basics to get a server started, with 100% of the actual logic living within the auth module
