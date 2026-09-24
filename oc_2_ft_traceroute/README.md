# ft_traceroute

A C implementation of the `traceroute` command.

## Description

`ft_traceroute` traces the network path between the local machine and a destination by displaying the intermediate hops and their response times.

The project is a reimplementation of `traceroute` using only the C standard library and low-level network functionality required by the subject.

## Features

* IPv4 addresses and hostnames
* FQDN handling
* Hop-by-hop route tracing
* Response time measurement
* `--help` option
* Error handling
* Makefile build system
* No external `traceroute` command is used

## Requirements

* C compiler
* Linux
* Make

## Compilation

```bash
make
```

## Usage

```bash
./ft_traceroute --help
./ft_traceroute <IPv4-address|hostname>
```

Example:

```bash
./ft_traceroute 8.8.8.8
```

## Bonus

No bonus features were implemented.
