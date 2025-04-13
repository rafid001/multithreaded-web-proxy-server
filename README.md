# Multithreaded Web Server

## Project Overview

This project implements a web server in Java using three different concurrency models: single-threaded, multi-threaded, and thread pool. It demonstrates the evolution of server architectures and showcases different approaches to handling concurrent client connections, providing a comprehensive comparison of performance, scalability, and resource utilization across these models.

## Technologies & Concepts Demonstrated

### Core Technologies

- **Java** - Core programming language
- **Java Networking API** - Socket programming for client-server communication
- **Java Concurrency Framework** - Thread management and synchronization
- **Java I/O** - Handling input/output streams for network communication

### Advanced Concepts

- **Socket Programming** - Low-level network communication using TCP/IP
- **Concurrent Programming** - Managing multiple simultaneous client connections
- **Thread Management** - Creation, lifecycle management, and synchronization
- **Thread Pooling** - Resource optimization through worker thread reuse
- **Consumer-Producer Pattern** - Used in the multi-threaded implementation
- **Java Functional Interfaces** - Leveraging Consumer interface for client handling
- **Resource Management** - Proper closing of connections using try-with-resources

## Architecture Overview

The project consists of three distinct implementations:

### 1. Single-Threaded Server

Located in the `SingleThreaded` directory, this implementation:

- Processes client requests sequentially in a blocking manner
- Uses a simple request-response model
- Demonstrates the baseline performance for comparison
- Limitations: Can only handle one client at a time, blocking architecture

### 2. Multi-Threaded Server

Located in the `Multithreaded` directory, this implementation:

- Creates a new thread for each incoming client connection
- Allows concurrent handling of multiple clients
- Uses Java's Thread class for parallel request processing
- Features a specialized Client implementation that can simulate high concurrency (100 parallel connections)
- Implements the Consumer functional interface for client request handling

### 3. Thread Pool Server

Located in the `ThreadPool` directory, this implementation:

- Uses Java's ExecutorService to maintain a fixed pool of worker threads
- Optimizes resource usage by reusing threads rather than creating new ones
- Implements a configurable thread pool size to fine-tune performance
- Prevents system resource exhaustion under high load
- Demonstrates proper thread pool lifecycle management

## Performance Characteristics

- **Single-Threaded**: Simple implementation, lowest concurrency, suitable for low-traffic scenarios
- **Multi-Threaded**: High concurrency, but potentially resource-intensive with unlimited thread creation
- **Thread Pool**: Balanced approach with controlled resource usage while maintaining good concurrency

## Key Technical Implementations

- **Socket Communication**: TCP/IP socket programming for reliable client-server communication
- **Thread Synchronization**: Ensuring thread safety in concurrent operations
- **Resource Management**: Proper handling of socket connections and I/O streams
- **Exception Handling**: Robust error detection and recovery
- **Timeout Management**: Implementing socket timeouts to prevent resource leaks
- **Functional Programming**: Using Java's functional interfaces for cleaner code

## Design Patterns Used

- **Factory Pattern**: Creation of client handlers
- **Strategy Pattern**: Different implementation strategies for server concurrency models
- **Producer-Consumer Pattern**: In the communication between server and client
- **Thread Pool Pattern**: For optimized resource management

## Skills Demonstrated

- Advanced Java programming
- Network programming and socket communication
- Concurrent and parallel programming
- Server architecture design and optimization
- Performance tuning and benchmarking
- Resource management and optimization
- Scalable system design

## Future Enhancements

This foundation could be extended to implement:

- Non-blocking I/O (NIO) for even greater scalability
- HTTP protocol support for web application hosting
- Load balancing across multiple server instances
- Performance metrics collection and monitoring
- Distributed systems communication patterns
