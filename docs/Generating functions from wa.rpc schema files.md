# .wa.rpc Schema

`.wa.rpc` are custom schemas similiar to goodle's protobuf, but with better performance.

```proto
// exaple.wa.rpc
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
