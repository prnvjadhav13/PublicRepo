# C++ Systems Programming Portfolio

A collection of focused C++ projects demonstrating practical systems-programming design, testing, and performance measurement on Linux.

## Projects

### [TcpEpollRequestBench](https://github.com/prnvjadhav13/TcpEpollRequestBench)

A C++23/Linux TCP request-response benchmark built around `epoll` and nonblocking I/O.

Highlights:

- Multiple independent `epoll` event loops using `SO_REUSEPORT`
- Safe handling of fragmented requests and partial nonblocking writes
- RAII ownership of file descriptors and memory mappings
- Configurable connection, request-size, and idle-time limits
- Concurrent client load generation with throughput and failure reporting
- Mapping data loaders based on `ifstream`, `mmap`, and zero-copy `mmap-view`

See the standalone project repository for build instructions, protocol details,
security boundaries, and benchmark methodology. The local
[`TcpEpollRequestBench/`](TcpEpollRequestBench/) directory is retained only as
a relocation notice for previously shared links.

### [TlsEpollRequestBench](https://github.com/prnvjadhav13/TlsEpollRequestBench)

A C++23/Linux TCP and TLS request-response benchmark for learning and measuring
TLS 1.2 and TLS 1.3 over a reusable `epoll` event-loop architecture, including
mutual TLS support and hardened transport policy.

## Notes

These are educational and benchmarking projects. Consult each standalone
repository's documentation and security guidance before production deployment.
