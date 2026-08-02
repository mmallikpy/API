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