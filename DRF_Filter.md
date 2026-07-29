# :snowflake: What is DRF Filtering?
```drf
Filtering হলো এমন একটি প্রক্রিয়া যেখানে client (Frontend/Postman/Mobile App) URL-এর query parameter ব্যবহার করে নির্দিষ্ট
data request করতে পারে।
```
# :snowflake: Why was it created?

Filtering তৈরি করা হয়েছে যাতে—

- Client অপ্রয়োজনীয় data না পায়।
- Database থেকে শুধুমাত্র দরকারি data retrieve করা যায়।
- API আরও flexible হয়।
- Performance improve হয়।

# :snowflake: What problem does it solve?

```drf
ধরুন আপনার Mobile model-এ 50,000 টি mobile আছে। Filtering না থাকলে সবগুলো mobile return করবে। কিন্তু user যদি শুধু 
Apple mobile দেখতে চায়?
Filtering থাকলে শুধু Apple mobile আসবে।
```

# :snowflake: Features of DRF Filtering
- Exact Filtering
- Range Filtering
- Greater Than Filtering
- Less Than Filtering
- Date Filtering
- Date Range Filtering
- Search Filtering
- Ordering Filtering
- Multiple Field Filtering
- Custom Filtering
- Boolean Filtering
- ForeignKey Filtering
- Choice Filtering
- Method Filtering
- Nested Filtering
- Dynamic Filtering

# :snowflake: Types of Filtering in DRF
- Manual Filtering
- django-filter
- SearchFilter
- OrderingFilter
- Custom Filter Backend