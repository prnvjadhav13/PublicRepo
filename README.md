# C++ Systems Programming Portfolio

A collection of focused C++ projects demonstrating practical systems-programming design, testing, and performance measurement on Linux.

## Featured project

### [TcpEpollRequestBench](TcpEpollRequestBench/)

A C++23/Linux TCP request-response benchmark built around `epoll` and nonblocking I/O.

Highlights:

- Multiple independent `epoll` event loops using `SO_REUSEPORT`
- Safe handling of fragmented requests and partial nonblocking writes
- RAII ownership of file descriptors and memory mappings
- Configurable connection, request-size, and idle-time limits
- Concurrent client load generation with throughput and failure reporting
- Mapping data loaders based on `ifstream`, `mmap`, and zero-copy `mmap-view`

See the project README for build instructions, protocol details, security boundaries, and benchmark methodology.

## Verification

GitHub Actions builds production and sanitizer variants, then runs a localhost client/server smoke test for the featured project.

## Notes

This is an educational and benchmarking project. It is not intended to be deployed as an unauthenticated Internet-facing service.
