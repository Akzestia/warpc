### Difference between different types of Task Status

```cpp
enum class TaskStatus : uint8_t {
  PENDING = 0,
  PROCESSING = 1,
  COMPLETED = 2,
  FAILED = 3,
  TIMEOUT = 4
};
```

### Pending

Task was successfully qued up inside execution queue.

### Processing

Task was sent with an async flag.

### Completed

Task was successfully completed.

### Failed

Task failed.

### Timeout

Task execution timedout.
