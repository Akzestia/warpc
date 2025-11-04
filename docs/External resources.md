### Creating and Using external resources inside rpc, via Meyers' singletons

```cpp
// Example rpc definition, that doesn't require
// access to any external resources
TaskStatus calc_compute_raw(rpc_call&, out_buff&) {
  out_buff = result;
  return TaslStatus::COMPLETED;
}
```

```cpp
// rpc definition with an external resource

// Meyers' singleton
struct DbProvider {
    static DbProvider& instance() {
        static DbProvider instance;
        return instance;
    }

    QueryResult query_user();
};

TaskStatus get_user_settings(rpc_call&, out_buff&){
  auto& db = DbProvider::instance();
  auto result = db.query_user(call.payload());

  out_buff = result;
  return TaslStatus::COMPLETED;
}
```
