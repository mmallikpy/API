# ----------------------------- API -----------------------------
### What is API?
```drf
API (application programming interface) is a defined set of rules that allows one piece of software to request data or
actions from another. It specifies how requests are made, what information is exchanged, and how responses are returned,
so systems can interact without exposing their internal code.
```
### How dose it's work?
```drf
An API works like a waiter in a restaurant, acting as the middleman between you (the client) and the kitchen (the server).

Here is the step-by-step process of how it works in real-time:
The 4-Step API Process
    1. The Request: You interact with an app (like searching for a flight). The app sends a structured request to a remote server via the API.
    2. The Delivery: The API securely delivers this request across the internet to the correct server.
    3. The Response: The server processes the request, looks up the data in its database, and formulates an answer.
    4. The Translation: The API takes that data back to your app, which translates it into a readable format on your screen.
```
### Based on Architectures how much API are available?
```drf
4 types API are available
```
|API Type|Best Used For|Data Format|
|------------|-------------------|-----|
|REST|Web applications and mobile apps|JSON, XML, HTML|
|GraphQL|Apps that need specific, fast data queries|JSON|
|SOAP|High-security enterprise systems and banks|XML only|
|RPC (gRPC)|High-performance, microservices communication|Protobuf, JSON|

### What is REST API?
```drf
A REST API (Representational State Transfer) is a popular architectural style used to build web services. It allows two computers to communicate over
the internet using standard web protocols like HTTP.Think of it as a set of rules that developers follow so their applications can talk to each other smoothly.
```
### How a REST API Works?
```drf
REST APIs work on a Client-Server model.
    1. The Client (your browser, phone app, or frontend code) sends a request.
    2. The Server (where the database lives) receives the request, processes it, and sends back data.
```
### The 4 Main HTTP Methods (CRUD Operations)
- #### GET
  ```drf
    Requests data from the server
  ```
- #### POST
  ```drf
    Sends new data to the server to create something. 
  ```
- #### PUT / PATCH
  ```drf
    Updates existing data on the server
  ```
- #### DELETE
  ```
    Removes data from the server
  ```
### Core principles of REST API?
- #### Client-Server Archicture
- #### Stateless
- #### Cacheable
- #### Uniform Interface
- #### Layered System
- #### Code on Demand

### What is API endpoints?
```drf
An API endpoint is a specific URL where an application sends requests to interact with another application or service.

Think of it like this:
    API = A waiter in a restaurant that takes your order and brings back your food.
    Endpoint = A specific menu item or counter where you place a particular order.
```
##### Examples
```drf
The complete endpoint URLs would be:

https://api.weather.com/current-weather
https://api.weather.com/forecast
https://api.weather.com/users
```

### Endpoints
  - #### Web applications endpoints
    ```drf
    A web application endpoint is a URL that returns an HTML page for a user to view in a browser.
    ```
    - ##### Examples
      ```drf
          https://example.com/
          https://example.com/login
          https://example.com/dashboard
          https://example.com/profile

      GET https://example.com/login

      # Output
      <html>
        <h1>Login</h1>
      </html>
      ```
  - #### API endpoints
    ```drf
    An API endpoint is a URL that returns data (usually JSON or XML) instead of a web page. It is designed for applications to communicate with each other.
    ```
    - ##### Examples
      ```drf
      https://api.example.com/users
      https://api.example.com/login
      https://api.example.com/products

      GET https://api.example.com/users
      
      # Output
      {
          "id": 1,
          "name": "Alice"
      }
      ``

# What is DRF?
```drf
DRF stands for Django REST Framework, which is a powerful, flexible, and open-source toolkit built on top of Django specifically
for creating Web APIs (Application Programming Interfaces)
```

### Serializers and dserializers
```drf
Serializers allow complex data such as querysets and model instances to be converted to native Python datatypes that can then
be easily rendered into JSON, XML or other content types. Serializers also provide deserialization, allowing parsed data to be
converted back into complex types, after first validating the incoming data.
```
### Core Architecture Components
    - Serializers
    - API Views & ViewSets
    - Routers
    - Authentication & Permissions
### Key Benefits
    - Browsable API
    - Massive Time Savings
    - Exceptional Scale

### Requests
### Responses
### Functions based view


### Class based view
  - APIView
    - get()
    - post()
    - get_object()
    - put()
    - delete()
  - Mixins
    - retriewModelMixin
    - ##### Create
      - CreateModelMixin
    - ##### Read
      - ListModelMixin
    - ##### Update
      UpdateModelMixin
    - ##### Delete
      - DestroyModelMixin
  - Generics
    - ListAPIView        For listing the objects
    - CreateAPIView      For creating the objects
    - RetrieveAPIView    For retrieveing a single object using pk
    - UpdateAPIView      For updateing a single object using pk
    - DestroyAPIView     For deleting an object using pk
    ###### Combination API view
    - ListCreateAPIView              For listing and createing objects
    - RetrieveUpdateAPIView          For retrieving & updating objects using pk
    - RetieveUpdateDestroyAPIview    For retrieving, updating & deleting objects using pk

  - Viewsets
    - viewsets.ViewSet
      - list()
      - create()
      - retrieve()
      - update()
      - delete()
        
    - viewsets.ModelViewSet

    - Routers  
    
##### Nested serializers
##### Pagination
  - PageNumberPagination
  - LimitOffsetPagination

  - GlobalPagination
  - CustomPagination
##### Filtering
  - Global Filter
  - Custom Filter
  - Search filter
