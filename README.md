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
    1. The Request: You interact with an app (like searching for a flight). The app sends a structured request to a remote
    server via the API.
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
A REST API (Representational State Transfer) is a popular architectural style used to build web services. It allows two computers
to communicate over the internet using standard web protocols like HTTP.Think of it as a set of rules that developers follow so
their applications can talk to each other smoothly.
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
    An API endpoint is a URL that returns data (usually JSON or XML) instead of a web page. It is designed for applications to
    communicate with each other.
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
### What is the Meta class?
```drf
The Meta class is an inner class inside a ModelSerializer that provides configuration to the serializer.

It tells Django REST Framework how the serializer should behave.
```
### Why do we use the Meta class?
```drf
ModelSerializer needs to know:

Which model should it use?
Which fields should be included?
Which fields should be read-only?
Which fields should be excluded?
Any extra configuration for fields?

All of this is defined inside the Meta class.
```

### What's the purpose of "fields" in ModelSerializer
```drf
In Django REST Framework (DRF), the fields attribute inside a ModelSerializer's Meta class explicitly controls which database
columns or properties are included in your API's JSON input and output.
```
### How many types of validation are there?
|Type|Purpose|
|------|-----|
|Built-in Validation|DRF/Model does it automatically|
| Field-level Validation|Validate a specific field|
|Object-level Validation|Validate multiple fields at once|
| Reusable Validator|Repeatedly using the same validation Custom validator function, RegexValidator, MinValueValidatorr|


### What validations does DRF do in ModelSerializer and what does it not do?
|Validation|Automatic?|
|-------|-------|
|required|✅|
|blank|✅|
| null                            | ✅                            |
| max_length                      | ✅                            |
| min_length (serializer field)   | ✅                            |
| Email format                    | ✅                            |
| URL format                      | ✅                            |
| Integer type                    | ✅                            |
| Float type                      | ✅                            |
| Decimal type                    | ✅                            |
| Boolean type                    | ✅                            |
| Date/Time format                | ✅                            |
| UUID format                     | ✅                            |
| choices                         | ✅                            |
| unique                          | ✅                            |
| UniqueConstraint                | ✅                            |
| Model field validators          | ✅                            |
| Custom business rules           | ❌                            |
| Cross-field validation          | ❌                            |
| Password confirmation           | ❌                            |
| Age > 18 (unless you define it) | ❌                            |
| Custom email domain             | ❌                            |
| Custom phone format             | ❌ (unless using a validator) |

### What is the Nested Serializer?
```drf
A Nested Serializer is a serializer inside another serializer.


It is used when one model is related to another model, and you want to return the related object's details, not just its ID.
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
    ```drf
    GenericAPIView provides the core functionality required by DRF mixins, such as get_queryset(), get_object(), and
    get_serializer().RetrieveModelMixin uses these methods to retrieve an object and serialize it. Without GenericAPIView,
    the mixin cannot work properly.
    ```
    - retriewModelMixin
      ```drf
          RetrieveModelMixin is used to retrieve (get) a single object from the database.
      ```
    - CreateModelMixin
        ```drf
        CreateModelMixin is used to create a single object in the database. It provides the built-in create() method,
        which validates the request data, saves the object, and returns a 201 Created response. It does not support
        bulk creation by default. To create multiple objects, you must use many=True and implement bulk creation logic
        if needed.
        ```    
    - ListModelMixin
      ```drf
      ListModelMixin is used to return a collection of objects. It provides the built-in list() method, which retrieves
      the queryset, serializes it with many=True, and returns the serialized data in the response. It is commonly used
      for endpoints like GET /students/.
      ```
    - UpdateModelMixin
      ```drf
      UpdateModelMixin is used to update an existing object. It provides the built-in update() method for full updates
      (PUT) and partial_update() for partial updates (PATCH). It retrieves the object, validates the incoming data, saves
      the changes, and returns the updated object in the response.
      ```
    - DestroyModelMixin
      ```drf
      DestroyModelMixin is used to delete a single object from the database. It provides the built-in destroy() method,
      which retrieves the object, calls perform_destroy(), deletes the object, and returns a 204 No Content response.
      ```
    #### Examples :
    - ##### serializers.py
      ```drf
      from rest_framework import serializers
      from snippets.models import BookStore
      
      class BookStoreSerializer(serializers.ModelSerializer):
            class Meta:
                model = BookStore
                fields = "__all__"
    
      ```
    - #### views.py
      ```drf
          from .models import BookStore
          from snippets.serializers import BookStoreSerializer
          from rest_framework import mixins, generics

          class bookViewMixins(mixins.ListModelMixin, mixins.CreateModelMixin, generics.GenericAPIView):
                queryset = BookStore.objects.all()
                serializer_class = BookStoreSerializer
    
                def get(self, request):
                    return self.list(request)
    
                def post(self,request):
                    return self.create(request)

          class bookViewMixinsDetail(mixins.RetrieveModelMixin, mixins.UpdateModelMixin, mixins.DestroyModelMixin, generics.GenericAPIView):
                queryset = BookStore.objects.all()
                serializer_class = BookStoreSerializer
    
                def get(self, request, pk):
                    return self.retrieve(request, pk)

                def put(self, request, pk):
                    return self.update(request, pk)
    
                def delete(self, request, pk):
                    return self.destroy(request, pk)
      ```
    - #### urls.py
      ```drf
        from django.urls import path
        from .views import *
        urlpatterns = [
            path("bookViewMixins/", bookViewMixins.as_view(), name="book view mixins"),
            path("bookViewMixins/<int:pk>", bookViewMixinsDetail.as_view(), name="book view mixins detail")
            ]
      ```
  - Generics
    - ListAPIView
      ```drf
      ListAPIView is a generic class-based view used to retrieve a list of objects. It handles GET requests and internally uses
      ListModelMixin with GenericAPIView. It automatically fetches the queryset, serializes it with many=True, and returns the
      list of objects. It also supports pagination, filtering, and ordering if configured.
      ```
    - CreateAPIView
      ```drf
      CreateAPIView is a generic class-based view used to create a new object. It handles POST requests and internally uses
      CreateModelMixin with GenericAPIView. It validates the request data using the serializer, saves the object, and returns
      a 201 Created response.
      ```
    - RetrieveAPIView
      ```drf
      RetrieveAPIView is a generic class-based view used to retrieve a single object. It handles GET requests for a specific
      resource and internally uses RetrieveModelMixin with GenericAPIView. It fetches the object by its lookup field
      (usually the primary key), serializes it, and returns the response.
      ```
    - UpdateAPIView
      ```drf
      UpdateAPIView is a generic class-based view used to update an existing object. It handles both PUT and PATCH requests
      and internally uses UpdateModelMixin with GenericAPIView. PUT performs a full update, while PATCH performs a partial update.
      ```
    - DestroyAPIView
      ```drf
      DestroyAPIView is a generic class-based view used to delete a single object. It handles DELETE requests and internally uses
      DestroyModelMixin with GenericAPIView. It retrieves the object, deletes it, and returns a 204 No Content response.
      ```
    ###### Combination API view
    - ListCreateAPIView
      ```drf
      ListCreateAPIView is a generic class-based view that combines listing and creating objects. It handles GET requests to return
      a list of objects and POST requests to create a new object. Internally, it uses ListModelMixin, CreateModelMixin, and
      GenericAPIView.
      ```
    - RetrieveUpdateAPIView
      ```drf
      RetrieveUpdateAPIView is a generic class-based view that combines retrieving and updating a single object. It handles GET
      requests to retrieve an object and PUT or PATCH requests to update it. Internally, it uses RetrieveModelMixin, UpdateModelMixin,
      and GenericAPIView.
      ```
    - RetieveUpdateDestroyAPIview
      ```drf
      RetrieveUpdateDestroyAPIView is a generic class-based view that combines retrieving, updating, and deleting a single object.
      It handles GET, PUT, PATCH, and DELETE requests. Internally, it uses RetrieveModelMixin, UpdateModelMixin, DestroyModelMixin,
      and GenericAPIView.
      ```

      #### Examples :
      - ##### serializers.py
        ```drf
            from rest_framework import serializers
            from employees.models import Employee
        
            class EmployeeSerilizer(serializers.ModelSerializer):
                class Meta:
                    model = Employee
                    fields = "__all__"
        ```
      - ##### views.py
        ```drf
              from rest_framework import generics
              from .serializers import StudentSerializers

            #------------1st way of generics---------------
                class StudentsGenericsList(generics.ListAPIView):
                    queryset = SutdentGenericsTest.objects.all()
                    serializer_class = StudentSerializers


                class StudentsGenericsCreate(generics.CreateAPIView):
                    queryset = SutdentGenericsTest.objects.all()
                    serializer_class = StudentSerializers

                class StudentsGenericsUpdate(generics.RetrieveAPIView, generics.UpdateAPIView):
                    queryset = SutdentGenericsTest.objects.all()
                    serializer_class = StudentSerializers
                    lookup_field = 'pk'

                class StudentsGenericsDelete(generics.RetrieveAPIView, generics.DestroyAPIView):
                    queryset = SutdentGenericsTest.objects.all()
                    serializer_class = StudentSerializers
                    lookup_field = 'pk'
          

            #------------2nd way of generics---------------
                class StudentsGenericsListCreateSecondway(generics.ListAPIView, generics.CreateAPIView):
                    queryset = SutdentGenericsTest.objects.all()
                    serializer_class = StudentSerializers
                    
                class StudentsGenericsUpdateDeleteSecondway(generics.RetrieveAPIView, generics.UpdateAPIView, generics.DestroyAPIView):
                    queryset = SutdentGenericsTest.objects.all()
                    serializer_class = StudentSerializers
                    lookup_field = 'pk'

            #------------3rd way of generics---------------
                class StudentsGenericsListCreate(generics.ListCreateAPIView):
                    queryset = SutdentGenericsTest.objects.all()
                    serializer_class = StudentSerializers
                    
                class StudentsGenericsListUpdateDelete(generics.RetrieveUpdateDestroyAPIView):
                    queryset = SutdentGenericsTest.objects.all()
                    serializer_class = StudentSerializers

        ```
        - ##### urls.py
        ```drf
                from django.contrib import admin
                from django.urls import path
                from .views import *

                urlpatterns = [
                    #------------1st way of generics---------------
                    path('studentgenericslist/', StudentsGenericsList.as_view(), name='studentgenerics-test-list'),
                    path('studentgenericscreate/', StudentsGenericsCreate.as_view(), name='studentgenerics-test-create'),
                    path('studentgenericsupdate/<int:pk>', StudentsGenericsUpdate.as_view(), name='studentgenerics-test-update'),
                    path('StudentsGenericsDelete/<int:pk>', StudentsGenericsDelete.as_view(), name='studentgenerics-test-delete'),
                
                    #------------2nd way of generics---------------
                    path('StudentsGenericsListCreateSecondway/', StudentsGenericsListCreateSecondway.as_view(), name='studentgenerics-test-List_Create_Secondway'),
                    path('StudentsGenericsUpdateDeleteSecondway/<int:pk>', StudentsGenericsUpdateDeleteSecondway.as_view(), name='studentgenerics-test-update_delete_Secondway'),
                
                    #------------3rd way of generics---------------
                    path('StudentsGenericsListCreate/', StudentsGenericsListCreate.as_view(), name='studentgenerics-test-List_Create'),
                    path('StudentsGenericsListUpdateDelete/<int:pk>', StudentsGenericsListUpdateDelete.as_view(), name='studentgenerics-test-List_Create_Update_Delete'),
                ]
        ```
        

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
