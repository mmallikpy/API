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
      ```
<hr>

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
<hr>

### Functions based view

<hr>

### Class based view

```drf
    Layer 1: Base API Views (2 Classes)
        - APIView
        - GenericAPIView
    
    Layer 2: Concrete Generic Views (9 Classes)
        - CreateAPIView
        - ListAPIView
        - RetrieveAPIView
        - UpdateAPIView
        - DestroyAPIView
        - ListCreateAPIView
        - RetrieveUpdateAPIView
        - RetrieveDestroyAPIView
        - RetrieveUpdateDestroyAPIView
    
    Layer 3: ViewSets (3 Classes)
        - ViewSet
        - GenericViewSet
        - ModelViewSet
        - ReadOnlyModelViewSet
    
    Layer 4: Mixinx (5 Classes)
        - CreateModelMixin
        - ListModelMixin
        - RetrieveModelMixin
        - UpdateModelMixin
        - DestroyModelMixin
        
        Note: Mixins can't run alone, It's need "GenericAPIView or GenericViewSet"
```



  - APIView
    - get
      ```drf
      The get() method handles HTTP GET requests. It is used to retrieve data from the database. It can return either
      a list of objects or a single object, depending on the API design.
      ```
    - post
      ```drf
      The post() method handles HTTP POST requests. It is used to create a new object. It validates the incoming data
      using a serializer, saves the object, and returns the created resource.
      ```
    - get_object
      ```drf
      get_object() is a helper method used to retrieve a single object from the database. It is commonly used in detail
      APIs before updating, retrieving, or deleting an object. If the object is not found, it usually raises a 404 error.
      ```
    - put
      ```drf
      The put() method handles HTTP PUT requests. It is used to perform a full update of an existing object. The client
      should send all required fields.
      ```
    - delete
      ```drf
      The delete() method handles HTTP DELETE requests. It is used to remove an existing object from the database.
      After successful deletion, it typically returns a 204 No Content response.
      ```
    #### Examples :
    - ##### serializers.py
      ```drf
      from rest_framework import serializers
      from snippets.models import BookStore, HumanInfo
      class HumanInfoSerializer(serializers.ModelSerializer):
          class Meta:
              model = HumanInfo
              fields = "__all__"
      ```
    - #### views.py
      ```drf
      from rest_framework.views import APIView
      from rest_framework.response import Response
      from rest_framework import status
      from django.http import Http404
      
      class HumanApiview(APIView):

          def get(self, request):
              human = HumanInfo.objects.all()
              serializer = HumanInfoSerializer(human, many=True)
              return Response(serializer.data, status=status.HTTP_200_OK)
        
          def post(self, request):
              serializer  = HumanInfoSerializer(data=request.data)
              if serializer.is_valid():
                  serializer.save()
                  return Response(serializer.data, status=status.HTTP_201_CREATED)
              return Response(serializer.errors, status=status.HTTP_400_BAD_REQUEST)

      class HumanApiviewDetail(APIView):

        def get_object(self, pk):
              try:
                  return HumanInfo.objects.get(pk=pk)
              except HumanInfo.DoesNotExist:
                  raise Http404
        
        def get(self, request, pk):
              human = self.get_object(pk)
              serializer = HumanInfoSerializer(human)
              return Response(serializer.data, status=status.HTTP_200_OK)
    
        def delete(self, request, pk):
              human = self.get_object(pk)
              human.delete()
              return Response(status=status.HTTP_204_NO_CONTENT)
            
        def put(self, request, pk):
              human = self.get_object(pk)
              serializer = HumanInfoSerializer(human, data=request.data)
      
              if serializer.is_valid():
                    serializer.save()
                    return Response(serializer.data, status=status.HTTP_200_OK)
              return Response(serializer.errors, status=status.HTTP_400_BAD_REQUEST)
      ```
    - #### urls.py
      ```drf
      from django.urls import path, include
      from .views import *

      urlpatterns = [
              path("humanViewApiview/", HumanApiview.as_view(), name="Human api view"),
              path("humanViewApiview/<int:pk>", HumanApiviewDetail.as_view(), name="Human api view"),
      ]
      ```
    - #### Limitations
      ```drf

        Compared to higher-level DRF classes:
        
        No automatic queryset handling
        No serializer integration by default
        No pagination
        No filtering
        No search
        No ordering
        No CRUD helpers (list, create, retrieve, etc.)
        More boilerplate code
      ```
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
            from .models import SutdentGenericsTest
        
            class StudentSerializers(serializers.ModelSerializer):
                class Meta:
                    model = SutdentGenericsTest
                    fields = "__all__"
        ```
      - ##### views.py
        ```drf
              from rest_framework import generics
              from .serializers import StudentSerializers
              from .models import SutdentGenericsTest

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
      - list
        ```drf
        The list() action is used to retrieve a collection of objects. It handles HTTP GET requests for a collection endpoint,
        such as /students/, and returns a serialized list of objects.
        ```
      - create
        ```drf
        The create() action is used to create a new object. It handles HTTP POST requests, validates the request data using a
        serializer, saves the object, and returns a 201 Created response.
        ```
      - retrieve
        ```drf
        The retrieve() action is used to retrieve a single object. It handles HTTP GET requests for a detail endpoint, such as
        /students/1/, fetches the object by its lookup field (usually the primary key), serializes it, and returns it.
        ```
      - update
        ```drf
        The update() action is used to perform a full update of an existing object. It handles HTTP PUT requests, validates the
        incoming data, updates the object, and returns the updated object.
        ```
      - delete
        ```drf
        The destroy() action is used to delete an existing object. It handles HTTP DELETE requests, removes the object from the
        database, and returns a 204 No Content response.
        ```
    #### Examples :
    - ##### serializers.py
      ```drf
      from rest_framework import serializers
      from .models import HumanInfo
      
      class HumanInfoSerializer(serializers.ModelSerializer):
      class Meta:
          model = HumanInfo
          fields = "__all__"
      ```
    - ##### views.py
      ```drf
      from rest_framework import viewsets
      from .serializers import HumanInfoSerializer
      from django.shortcuts import get_object_or_404
      from rest_framework.response import Response
      from .models import HumanInfo

      class humanViewset(viewsets.ViewSet):

        def list(self, request):
            queryset = HumanInfo.objects.all()
            serializer_class = HumanInfoSerializer(queryset, many=True)
            return Response(serializer_class.data)
    
        def create(self, request):
            serializer_class = HumanInfoSerializer(data = request.data)
            if serializer_class.is_valid():
                serializer_class.save()
                return Response(serializer_class.errors)
    
        def retrieve(self, request, pk=None):
            human = get_object_or_404(HumanInfo, pk=pk)
            serializer = HumanInfoSerializer(human)
            return Response(serializer.data, status=status.HTTP_200_OK)
    
        def update(self, request, pk):
            human = get_object_or_404(HumanInfo, pk=pk)
            serializer = HumanInfoSerializer(human, data=request.data)
            if serializer.is_valid():
                serializer.save()
                return Response(serializer.data)
            return Response(serializer.errors)
    
        def delete(self, request, pk):
            human = get_object_or_404(HumanInfo, pk=pk)
            human.delete()
            return Response(status=status.HTTP_204_NO_CONTENT)

      ```
    - ##### urls.py
      ```drf
      from django.urls import path
      from .views import *
      urlpatterns = [
            path("humanViewset/", humanViewset.as_view({'get': 'list', 'post':'create'}), name="Human viewserts"),
            path("humanViewset/<int:pk>/", humanViewset.as_view({'get':'retrieve', 'patch':'update', 'put':'update', 'delete':'delete'}), name="Human viewserts detail"),
        ]
      ```

    - #### Router
      ```drf
      from rest_framework.routers import DefaultRouter

      router = DefaultRouter()
      router.register("humans", HumanViewSet, basename="human")
        
      urlpatterns = router.urls
      ```

    - #### Limitations
      ```drf
      Compared to GenericViewSet and ModelViewSet:

        No automatic queryset handling
        No serializer integration by default
        No pagination
        No filtering
        No search
        No ordering
        No CRUD implementation (you must write actions yourself)
      ```
<hr>

- viewsets.GenericViewSet
  - #### What is it?
    ```drf
        enericViewSet is a DRF class that combines GenericAPIView and ViewSet. It provides generic features
        (queryset, serializer, filtering, pagination, etc.) but does not implement CRUD actions by itself.
    ```
  - #### What problem does it solve?
    ```drf
        Without GenericViewSet, you would have to:
            Write custom actions manually.
            Add filtering, pagination, serializer handling yourself.
        It provides these features while letting you choose only the CRUD actions you need.
    ```
    - #### What features does it provide?
      ```drf
        queryset
        serializer_class
        get_queryset()
        get_serializer()
        get_object()
        Filtering
        Searching
        Ordering
        Pagination
        Permissions
        Authentication
        Routers support
        Can use DRF Mixins (ListModelMixin, CreateModelMixin, etc.)
      ```
    - #### serializers.py
      ```drf
      from rest_framework import serializers
      from .models import HumanInfo
      
      class HumanInfoSerializer(serializers.ModelSerializer):
      class Meta:
          model = HumanInfo
          fields = "__all__"
      ```
    - #### views.py
      ```drf
        from rest_framework import viewsets, mixins
        from .models import HumanInfo
        from .serializers import HumanInfoSerializer
        
        class HumanViewSet( mixins.ListModelMixin, mixins.CreateModelMixin, viewsets.GenericViewSet):
            queryset = HumanInfo.objects.all()
            serializer_class = HumanInfoSerializer
        
            def get(self, request):
                return self.list(request)
            
            def post(self, request):
                return self.create(request)
        
        class HumanViewSetdetails(mixins.RetrieveModelMixin, mixins.UpdateModelMixin, mixins.DestroyModelMixin, viewsets.GenericViewSet):
            queryset = HumanInfo.objects.all()
            serializer_class = HumanInfoSerializer
        
            def get(self, reqeust, pk):
                return self.retrieve(reqeust, pk)
            
            def put(self, reqeust, pk):
                return self.update(reqeust, pk)
            
            def delete(self, reqeust, pk):
                return self.destroy(reqeust, pk)
      ```
    - #### urls.py
      ```drf
      from django.urls import path
      from .views import *
      urlpatterns = [
            path("humanViewSetx/", HumanViewSet.as_view({'get': 'list', 'post':'create'}), name="Human api view set"),
            path("humanViewSetx/<int:pk>", HumanViewSetdetails.as_view({'get': 'retrieve', 'put':'update', 'delete':'destroy'}), name="Human api view set details"),
      ]
      ```

    - viewsets.ModelViewSet

    - Routers  
<hr>

##### Nested serializers
##### Pagination
- ##### What is it?
  ```drf
  Pagination is a feature in Django REST Framework (DRF) that divides a large queryset into smaller pages and returns
  only a limited number of records in each API response. Instead of returning all records at once, the API returns a
  subset (page) along with information about other pages.
  ```
- ##### Why was it created?
  ```drf
  Pagination was created to efficiently handle APIs that contain a large amount of data.
  Without pagination, an API may need to send thousands or millions of records in a single
  response, making it slow and inefficient.
  ```
- ##### Built-in Pagination Classes
  - GlobalPagination
  - PageNumberPagination
    ```drf
    PageNumberPagination is the default pagination class in Django REST Framework (DRF) that divides a queryset
    into pages and lets clients request a specific page using a page number.
    ```
    - Examples
      ```drf
      from rest_framework.pagination import PageNumberPagination
      from rest_framework.response import Response

      class CustomPagination(PageNumberPagination):
        page_size_query_param = "page_size"
        page_query_param = "page-num"
        page_size = 5
        max_page_size = 5

        def get_paginated_response(self, data):
            return Response({
                'next': self.get_next_link(),
                'previous': self.get_previous_link(),
                'count': self.page.paginator.count,
                'page_size': self.page_size,
                'results': data
            })
      ```
    - common attributes
      ```drf
            page_size
            page_query_param
            page_size_query_param
            max_page_size
            last_page_strings
      ```
- LimitOffsetPagination
  - #### What is it?
    ```drf
        LimitOffsetPagination is a built-in pagination class in Django REST Framework (DRF) that paginates data using limit
        (how many records to return) and offset (how many records to skip).
    ```
    - Example
      ```drf
      from rest_framework.pagination import LimitOffsetPagination
      from rest_framework.response import Response


      class LimitOffsetCustomPagination(LimitOffsetPagination):
            default_limit = 5
            limit_query_param = "limit"
            offset_query_param = "offset"
            max_limit = 100
        
            def get_paginated_response(self, data):
                return Response({
                    'links': {
                        'next_page': self.get_next_link(),
                        'previous_page': self.get_previous_link(),
                    },
                    'count': self.count,
                    'limit': self.limit,
                    'offset': self.offset,
                    'results': data
                })
      ```
    - Common attribute
      ```drf
          default_limit → Default number of records.
          limit_query_param → Name of the limit parameter.
          offset_query_param → Name of the offset parameter.
          max_limit → Maximum allowed limit.
      ```

    
  - CursorPagination
    - #### What is it?
      ```drf
          CursorPagination is a built-in pagination class in Django REST Framework (DRF) that paginates data using a cursor
          instead of page numbers or offsets. A cursor is an encoded token that tells the API where to continue fetching records.
      ```
    - #### Why was it created?
      ```drf
          It was created to solve the problems of PageNumberPagination and LimitOffsetPagination when working with:

            Very large datasets
            Frequently changing data
            Infinite scrolling
      ```
    - #### What problem does it solve?
      ```drf
          With page numbers or offsets:
            New records may be inserted while users are browsing.
            Records can be duplicated or skipped.
            Large offsets become slow on large databases.
    
            CursorPagination solves these problems by using a cursor that always continues from the last fetched record.
      ```
    - #### Common Attributes
      ```drf
        page_size
        cursor_query_param
        ordering
        page_size_query_param
        max_page_size
      ```
    - #### Example
      ```drf
      from rest_framework.pagination import CursorPagination
      from rest_framework.response import Response


      class CursorCustomCursorPagination(CursorPagination):
            page_size = 5
            ordering = "-price"
            cursor_query_param = "cursor"
            page_size_query_param = "page_size"
            max_page_size = 100
        
            def get_paginated_response(self, data):
                return Response({
                    "links": {
                        "next_page": self.get_next_link(),
                        "previous_page": self.get_previous_link(),
                    },
                    "page_size": self.page_size,
                    "ordering": self.ordering,
                    "results": data
                })
      ```

##### Filtering
  - Global Filter
  - Custom Filter
  - Search filter

<hr>

| Class              |      CRUD      | Filtering | Pagination |  Search  | Ordering | Permissions | Authentication | Throttling |
| ------------------ | :------------: | :------------: | :------------: | :------------: | :------------: | :------------: | :------------: | :--------: |
| `APIView`          |    ❌ Manual    |  ❌ Manual |  ❌ Manual  | ❌ Manual | ❌ Manual |      ✅      |        ✅       |      ✅     |
| `ViewSet`          |    ⚠️ Manual   |  ❌ Manual |  ❌ Manual  | ❌ Manual | ❌ Manual |      ✅      |        ✅       |      ✅     |
| `GenericAPIView`   |   ⚠️ Partial   |     ✅     |      ✅     |     ✅    |     ✅    |      ✅      |        ✅       |      ✅     |
| `GenericViewSet`   | ⚠️ With Mixins |     ✅     |      ✅     |     ✅    |     ✅    |      ✅      |        ✅       |      ✅     |
| **`ModelViewSet`** |   ✅ Automatic  |     ✅     |      ✅     |     ✅    |     ✅    |      ✅      |        ✅       |      ✅     |


#### Disalbe DRF browsable api

```drf
    REST_FRAMEWORK = {
        'DEFAULT_RENDERER_CLASSES': ['rest_framework.renderers.JSONRenderer'],
    }
```


# Throttling
### UserRateThrottle
```drf
serRateThrottle প্রতিটি Login করা User-এর জন্য আলাদা request limit সেট করে।
এটি User ID (অর্থাৎ request.user) ব্যবহার করে user-কে শনাক্ত করে।

অর্থাৎ—
- Login করা user → ✅ Throttle প্রযোজ্য
- Login না করা user → ❌ এই throttle কাজ করবে না
```
#### Example
```drf
In settings.py

REST_FRAMEWORK = {
    "DEFAULT_THROTTLE_CLASSES": [
        "rest_framework.throttling.UserRateThrottle",
    ],

    "DEFAULT_THROTTLE_RATES": {
        "user": "5/min",
    }
}
```

### AnonRateThrottle
```drf
AnonRateThrottle হলো এমন একটি Throttle Class যা শুধুমাত্র Anonymous (Unauthenticated)
user-এর request limit করে।

অর্থাৎ—

Login করা user → ❌ এই throttle প্রযোজ্য নয়
Login না করা user → ✅ এই throttle প্রযোজ্য
```
#### Example
```drf
In settings.py

REST_FRAMEWORK = {
    "DEFAULT_THROTTLE_CLASSES": [
        "rest_framework.throttling.AnonRateThrottle",
    ],

    "DEFAULT_THROTTLE_RATES": {
        "anon": "5/min",
    }
}
```
#### যদি দুটো একসাথে ব্যবহার করি?
```drf
In settings.py

REST_FRAMEWORK = {
    "DEFAULT_THROTTLE_CLASSES": [
        "rest_framework.throttling.AnonRateThrottle",
        "rest_framework.throttling.UserRateThrottle",
    ],

    "DEFAULT_THROTTLE_RATES": {
        "anon": "10/min",
        "user": "100/min",
    }
}
```

### ScopedRateThrottle
```drf
ScopedRateThrottle হলো DRF-এর একটি Built-in Throttle Class, যা নির্দিষ্ট API বা 
API Group-এর জন্য আলাদা Rate Limit সেট করতে ব্যবহৃত হয়।

অর্থাৎ, একই Project-এর বিভিন্ন API-এর জন্য আপনি ভিন্ন ভিন্ন request limit দিতে পারবেন।
```
#### Example
```drf

REST_FRAMEWORK = {
    "DEFAULT_THROTTLE_CLASSES": [
        "rest_framework.throttling.ScopedRateThrottle",
    ],

    "DEFAULT_THROTTLE_RATES": {
        "products": "1000/hour",
        "login": "5/min",
        "payment": "10/hour",
    }
}



from rest_framework.viewsets import ModelViewSet
from rest_framework.throttling import ScopedRateThrottle

class ProductViewSet(ModelViewSet):
    throttle_classes = [ScopedRateThrottle]
    throttle_scope = "products"


class LoginAPIView(APIView):
    throttle_classes = [ScopedRateThrottle]
    throttle_scope = "login"


class PaymentAPIView(APIView):
    throttle_classes = [ScopedRateThrottle]
    throttle_scope = "payment"

```

### AnonRateThrottle vs UserRateThrottle vs ScopedRateThrottle

| Feature         | AnonRateThrottle | UserRateThrottle   | ScopedRateThrottle  |
| --------------- | ---------------- | ------------------ | ------------------- |
| কাদের জন্য      | Anonymous User   | Authenticated User | নির্দিষ্ট API/Scope |
| শনাক্তকরণ       | IP Address       | User ID            | User/IP + Scope     |
| আলাদা API Limit | ❌                | ❌                  | ✅                   |
| Public API      | ✅                | ❌                  | ✅                   |
| Login API       | ❌                | ❌                  | ✅                   |
| Payment API     | ❌                | ❌                  | ✅                   |
