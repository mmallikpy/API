# ----------------------------- API -----------------------------
### What is API?
### How dose it's work?
### What is REST API?
### Core principles of REST API?
- #### Stateless
- #### Client-Server Archicture
### What is API endpoints?
### HTTP Request methods
- #### GET
- #### POST
- #### PUT
- #### DELETE
### Endpoints
  - #### Web applications endpoints
  - #### API endpoints

### Serializers and dserializers
  - #### Model serializers
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
