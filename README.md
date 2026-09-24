# 42 Madrid — Systems & Software Engineering Portfolio

Centralized repository containing core curriculum and advanced systems engineering projects developed at **42 Madrid**. Focus areas include low-level C programming, POSIX system calls, network programming, non-blocking I/O, concurrency, and modular C++ design.

---

## 🛠️ Quick Navigation: Core Projects

| Project | Stack | Key Architectural Focus | Core Technical Skills |
| :--- | :--- | :--- | :--- |
| [**webserv**](https://github.com/KarmaFaber/42_School/tree/main/14_webserv) | `C++98` `Sockets` | Non-blocking HTTP/1.1 server (RFC 7230), I/O multiplexing (`select`/`poll`/`epoll`) | Network protocols, event-driven architecture, CGI, config parsing |
| [**minishell**](https://github.com/KarmaFaber/42_School/tree/main/9_minishell) | `C` `POSIX` | Unix CLI interpreter with pipes, redirections, and process execution | Process lifecycle (`fork`/`execve`), file descriptors, signal handling, AST |
| [**philosophers**](https://github.com/KarmaFaber/42_School/tree/main/8_philosophers) | `C` `pthreads` | Synchronization solution for the Dining Philosophers problem | Multithreading, mutexes, deadlock prevention, race condition mitigation |
| [**ft_ping**](https://github.com/KarmaFaber/42_School/tree/main/oc_1_ft_ping) | `C` `Raw Sockets` | Low-level network diagnostic tool following `inetutils-2.0` | ICMP protocol, raw socket operations, RFC 1071 checksum calculation |
| [**ft_traceroute**](https://github.com/KarmaFaber/42_School/tree/main/oc_2_ft_traceroute) | `C` `Networking` | Packet path tracing utility analyzing network hops and latency | IPv4 TTL manipulation, DNS reverse lookup, ICMP response parsing |
| [**Inception**](https://github.com/KarmaFaber/42_School/tree/main/13_inception) | `Docker` `DevOps` | Multi-container isolated microservices infrastructure | Docker Compose, TLS/SSL termination, Nginx reverse proxy, MariaDB |
| [**push_swap**](https://github.com/KarmaFaber/42_School/tree/main/7_push_swap) | `C` `Algorithms` | Data sorting on dual stacks with constrained instruction sets | Algorithmic optimization, time/space complexity, data structures |
| [**pipex**](https://github.com/KarmaFaber/42_School/tree/main/5_pipex) | `C` `Unix` | Emulation of the Unix pipe mechanism (`< in cmd1 \| cmd2 > out`) | Inter-process communication (IPC), unidirectional pipes, dup2 redirection |

---

## 💻 Systems & Infrastructure Projects

### [webserv (C++)](https://github.com/KarmaFaber/42_School/tree/main/14_webserv)
*Fully compliant, concurrent HTTP/1.1 server built from scratch without external network libraries.*
- **System Requirements:** Multiplex non-blocking I/O operations across multiple client sockets; parse complex Nginx-style server configurations; handle file uploads and static routing; execute external scripts via standard Common Gateway Interface (CGI).
- **Engineering Skills:** Sockets API, non-blocking network I/O (`epoll`/`select`), state machines for HTTP request chunking, signal and pipe management for CGI isolation, RFC 7230 validation.

### [minishell (C)](https://github.com/KarmaFaber/42_School/tree/main/9_minishell)
*A custom, POSIX-compliant command-line interpreter recreating Bash behaviors.*
- **System Requirements:** Complete execution loop: lexical analysis, command parsing, environment variable expansion, recursive pipe chains, file redirections (`<`, `>`, `>>`, `<<`), and asynchronous terminal signal handling (`SIGINT`, `SIGQUIT`).
- **Engineering Skills:** Process spawning (`fork`), binary execution (`execve`), process tracking (`waitpid`), file descriptor duplicates (`dup2`), memory safety with Valgrind verification.

### [philosophers (C)](https://github.com/KarmaFaber/42_School/tree/main/8_philosophers)
*Concurrent system simulation solving the Dining Philosophers problem.*
- **System Requirements:** Simulate multiple agents competing for limited shared resources without deadlocks, resource starvation, or data races under millisecond timing constraints.
- **Engineering Skills:** POSIX threads (`pthread_create`, `pthread_join`), mutex synchronization (`pthread_mutex`), atomic state evaluation, memory sanitization with Helgrind and DRD.

### [ft_ping & ft_traceroute (C)](https://github.com/KarmaFaber/42_School/tree/main/oc_1_ft_ping)
*Low-level packet manipulation tools interacting directly with Layer 3 (Network).*
- **System Requirements:** Construct and parse raw network frames; handle ICMP Echo Requests and Replies; manipulate IP Header fields (TTL values); calculate exact round-trip network latency.
- **Engineering Skills:** Raw sockets (`SOCK_RAW`), manual bitwise header serialization, RFC 1071 checksum implementation, system socket options (`setsockopt`).

### [Inception (Docker)](https://github.com/KarmaFaber/42_School/tree/main/13_inception)
*Multi-service infrastructure orchestrating isolated system containers.*
- **System Requirements:** Build a production-like local infrastructure from base Alpine/Debian images using `docker-compose`; establish encrypted network channels using TLSv1.2/TLSv1.3; configure volume persistence and network isolation without automated quick-start tools.
- **Engineering Skills:** Dockerfile optimization, systemd/init virtualization, persistent storage management, self-signed SSL/TLS termination, secure service-to-service communication.

---

## 🧩 Foundational Software Architecture & C++ Modules

### [C++ Modules 00 to 09](https://github.com/KarmaFaber/42_School/tree/main/12_CPPs)
*Progressive technical deep-dive into Modern C++ fundamentals, OOP rigor, and generic programming.*
- **CPP 00–04:** Orthodox Canonical Class Form, memory references vs. pointers, const-correctness, static polymorphism (overloading), dynamic subtype polymorphism, and abstract interfaces.
- **CPP 05–08:** Robust exception handling patterns (`try`/`catch`), explicit type casting mechanics (`static_cast`, `dynamic_cast`, `reinterpret_cast`, `const_cast`), class and function templates.
- **CPP 09:** Real-world Standard Template Library (STL) algorithms and container design patterns (`std::map`, `std::deque`, `std::stack`) with strict time-complexity constraints.

### Foundational Algorithms & Low-Level C Modules
- **[Push_Swap](https://github.com/KarmaFaber/42_School/tree/main/7_push_swap):** Custom sorting algorithm optimizing instruction counts using dual stacks and mechanical index mappings.
- **[Pipex](https://github.com/KarmaFaber/42_School/tree/main/5_pipex):** Pipeline emulation using unidirectional POSIX pipes, `fork`, and file descriptor redirection.
- **[Get_Next_Line](https://github.com/KarmaFaber/42_School/tree/main/4_GetNextLine):** Buffered stream parser reading arbitrary file descriptors line by line with dynamic heap buffers and zero memory leakage.
- **[ft_printf](https://github.com/KarmaFaber/42_School/tree/main/3_printf):** Variadic argument handling (`va_list`) and formatted string parsing reproducing `printf` behaviors.
- **[Libft](https://github.com/KarmaFaber/42_School/tree/main/1_libft):** Recreation of essential standard C library routines, dynamic string manipulations, and linked-list data structures.

---

## 🧪 Quality Assurance & Test Suites

Custom automated test suites built to ensure zero regressions, enforce memory hygiene, and detect edge-case failures across projects:

- **[test_parse_webserv](https://github.com/KarmaFaber/test_parse_webserv):** Automated testing framework injecting malformed tokens, broken scopes, and invalid directives to validate server configuration parsers.
- **[ft_printf_test](https://github.com/KarmaFaber/ft_printf_test):** Differential testing harness running edge-case specifiers, precision truncations, and boundary limits against native `glibc` implementations.
- **[GetNextLine_test](https://github.com/KarmaFaber/GetNextLine_test):** Automated pipeline testing file descriptor starvation, arbitrary read buffer limits (`1B` to `10MB`), binary inputs, and file access edge conditions under continuous Valgrind monitoring.

---

## 🤖 AI Mentorship & Engineering Workflow

AI tools are integrated into the engineering lifecycle strictly under a **Socratic mentor–student model**:
- **Diagnostic Mentorship:** LLMs act as technical sounding boards for architectural validation, edge-case discovery, and RFC interpretation without generating unverified boilerplate.
- **Verification Strategy:** Automated unit tests, integration harnesses, and Valgrind memory audits are executed locally on native Linux environments to independently verify code correctness and system stability.