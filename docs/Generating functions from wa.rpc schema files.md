# wa.rpc Schema

```proto
message RequestHeader {
    payload_len: u32
    route: u8
    flags: u8
}

message ResponseHeader {
    payload_len: u32
    task_status: u8
    flags: u8
    array_field: string[]
}

```

# Supported types

- `string`
- `bool`
- `u8`
- `u16`
- `u32`
- `u64`
- `i16`
- `i32`
- `i64`
- `f32`
- `f65`
- `array[]`

```proto
message Types {
    x: string
    x: bool
    x: u8
    x: u16
    x: u32
    x: u64
    x: i16
    x: i32
    x: i64
    x: f32
    x: f64

    array: u8[]
    array: bool[]
    array: f64[]
    ...
}
```
