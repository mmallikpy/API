# Interview Questions
## Basic
    Model কী?
    ORM কী?
    Migration কী?
    models.Model কী?

    Serializer কী?
    ModelSerializer কী?
    Serialization এবং Deserialization-এর পার্থক্য কী?

    Serializer কী?
    ModelSerializer কী?
    এদের মধ্যে পার্থক্য কী?

    Validation কী?
    is_valid() কী করে?
    validated_data কী?

    APIView কী?
    APIView এবং Django View-এর পার্থক্য কী

    Filtering কী?
    Filtering এবং Searching-এর পার্থক্য কী?
    DjangoFilterBackend কী?

## Intermediate
    null=True এবং blank=True-এর পার্থক্য কী?
    ForeignKey এবং OneToOneField-এর পার্থক্য কী?
    _meta কী কাজে লাগে?

    Serializer এবং ModelSerializer-এর পার্থক্য কী?
    serializer.data এবং validated_data-এর পার্থক্য কী?
    many=True কেন লাগে?

    ModelSerializer কীভাবে Field Generate করে?
    create() Override কখন করবে?
    update() Override কখন করবে?

    validate_<field>() এবং validate()-এর পার্থক্য কী?
    serializer.errors কীভাবে কাজ করে?
    Built-in Validation কোথা থেকে আসে?

    dispatch() কী করে?
    initialize_request() কী করে?
    request.data এবং request.POST-এর পার্থক্য কী?
    Manual Filtering কীভাবে কাজ করে?
    filterset_fields কী?
    FilterSet কী?
## Advanced
    ModelBase কী?
    Manager এবং QuerySet কীভাবে কাজ করে?
    Migration কীভাবে Model-এর পরিবর্তন শনাক্ত করে?
    select_related() এবং prefetch_related() কখন ব্যবহার করবে?

    to_representation() কী করে?
    to_internal_value() কী করে?
    SerializerMethodField কখন ব্যবহার করবে?
    create() এবং update() কীভাবে Override করবে?
    Nested Serializer-এর Performance কীভাবে Optimize করবে?

    ModelSerializer-এর Automatic Validation কীভাবে কাজ করে?
    Serializer কি Model ছাড়াই ব্যবহার করা যায়?
    ModelSerializer কি Serializer-এর Subclass?

    উত্তর: হ্যাঁ। ModelSerializer মূলত Serializer-এর উপর নির্মিত একটি Specialized Class, যা Model Metadata ব্যবহার করে অতিরিক্ত সুবিধা দেয়।

    Validation-এর Execution Order কী?
    to_internal_value() কী করে?
    Serializer Validation, Model Validation এবং Database Constraint-এর মধ্যে পার্থক্য কী?

    APIView-এর Lifecycle ব্যাখ্যা করো।
    Authentication, Permission এবং Throttle কোন Order-এ Execute হয়?
    কেন Response ব্যবহার করা হয় JsonResponse-এর পরিবর্তে?

    QuerySet Lazy Evaluation কী?
    Filtering-এর সময় SQL কখন Execute হয়?
    Custom Filter Backend কীভাবে তৈরি করবে?
    Filtering-এর Performance কীভাবে Optimize করবে?