# Polyphony - Easy Concurrency for Ruby

[![Gem Version](https://badge.fury.io/rb/polyphony-http.svg)](http://rubygems.org/gems/polyphony-http)
[![Modulation Test](https://github.com/digital-fabric/polyphony-http/workflows/Tests/badge.svg)](https://github.com/digital-fabric/polyphony-http/actions?query=workflow%3ATests)
[![MIT licensed](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/digital-fabric/polyphony-http/blob/master/LICENSE)

[DOCS](https://dfab.gitbook.io/polyphony) |
[EXAMPLES](examples)

> Polyphony \| pəˈlɪf\(ə\)ni \| _Music_ - the style of simultaneously combining a number of parts, each forming an individual melody and harmonizing with each other.

## What is Polyphony

Polyphony is a library for building concurrent applications in Ruby. Polyphony harnesses the power of [Ruby fibers](https://ruby-doc.org/core-2.5.1/Fiber.html) to provide a cooperative, sequential coprocess-based concurrency model. Under the hood, Polyphony uses [libev](https://github.com/enki/libev) as a high-performance event reactor that provides timers, I/O watchers and other asynchronous event primitives.

Polyphony makes it possible to use normal Ruby built-in classes like `IO`, and `Socket` in a concurrent fashion without having to resort to threads. Polyphony takes care of context-switching automatically whenever a blocking call like `Socket#accept` or `IO#read` is issued.

## Features

* **Full-blown, integrated, high-performance HTTP 1 / HTTP 2 / WebSocket server
  with TLS/SSL termination, automatic ALPN protocol selection, and body
  streaming**.
* Co-operative scheduling of concurrent tasks using Ruby fibers.
* High-performance event reactor for handling I/O events and timers.
* Natural, sequential programming style that makes it easy to reason about
  concurrent code.
* Abstractions and constructs for controlling the execution of concurrent code:
  coprocesses, supervisors, cancel scopes, throttling, resource pools etc.
* Code can use native networking classes and libraries, growing support for
  third-party gems such as `pg` and `redis`.
* Use stdlib classes such as `TCPServer`, `TCPSocket` and 
* HTTP 1 / HTTP 2 client agent with persistent connections.
* Competitive performance and scalability characteristics, in terms of both
  throughput and memory consumption.

## Prior Art

Polyphony draws inspiration from the following, in no particular order:

* [nio4r](https://github.com/socketry/nio4r/) and [async](https://github.com/socketry/async)
  (Polyphony's C-extension code is largely a spinoff of
  [nio4r's](https://github.com/socketry/nio4r/tree/master/ext))
* [EventMachine](https://github.com/eventmachine/eventmachine)
* [Trio](https://trio.readthedocs.io/)
* [Erlang supervisors](http://erlang.org/doc/man/supervisor.html) (and actually,
  Erlang in general)

## Documentation

The complete documentation for Polyphony could be found on the
[Polyphony website](https://dfab.gitbook.io/polyphony).
