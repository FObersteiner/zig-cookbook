## UDP Echo

Similar to the TCP server example, this program will listen on the specified
IP address and port, but for UDP datagrams this time. If data is received,
it will be echoed back to the sender's address.

Although `std.net` is mostly focused on abstractions for TCP (so far), we can still
make use of socket programming to communicate via UDP.

```zig
{{#include ../src/04-03.zig }}
```

After starting the program, test as follows with `nc`, using the `-u` flag for UDP:

```bash
echo "hello zig" | nc -u localhost <port>
```
