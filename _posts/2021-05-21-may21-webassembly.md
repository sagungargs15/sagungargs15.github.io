---
layout: post
title: "May21: Webassembly Basics & Python"
date: 2021-05-21 23:59:59 -0000
categories: programming webassembly
author: "Sagun Garg"
tags: polyglot programming webassembly
---


# What is WebAssembly?

Quoting [the WebAssembly site](https://webassembly.org/):

> WebAssembly (abbreviated Wasm) is a binary instruction format for a
> stack-based virtual machine. Wasm is designed as a portable target
> for compilation of high-level languages like C/C++/Rust, enabling
> deployment on the web for client and server applications.

About speed:

> WebAssembly aims to execute at native speed by taking advantage of
> [common hardware
> capabilities](https://webassembly.org/docs/portability/#assumptions-for-efficient-execution)
> available on a wide range of platforms.

About safety:

> WebAssembly describes a memory-safe, sandboxed [execution
> environment](https://webassembly.org/docs/semantics/#linear-memory) […].


# Update on WebAssembly

- WebAssembly’s first major version focused on the browser. 

- WebAssembly is now expanding its focus beyond just the browser with a series of features designed to enable its vision of a portable binary format on many platforms, bringing great benefits in tooling and language-agnosticity.

- A large number of non-browser runtimes have appeared with different areas of focus (performance, size, and more).

- The Wasmtime runtime recently implemented the reference types proposal, allowing Wasm modules to properly interact with external host objects. 

- This means better integration between a Wasm module and the outside world (DOM APIs when loaded inside a Webpage, or with a database API when instantiated on a server).

- Thanks to the `wasm-smith` test case generator, hard-to-find bugs in the `wasmparser` Rust crate have been fixed
Next candidate features are type imports, interface types, module linking, and more.

- WebAssembly recently became a World Wide Web Consortium recommendation and the fourth language to run natively in browsers, after HTML, CSS, and JavaScript. 

- While WebAssembly’s first major version focused on the browser, WebAssembly is now focusing to non-browser environments to fulfill a variety of computational tasks, where sandboxing, portability or performance are essential. 

- In this context, non-browser-based WebAssembly runtimes are being developed in miscellaneous languages, (Wasmtime and wasmer in Rust, GraalWasm in Java, Lucet in Rust, py-wasm in Python, swam in Scala, and more), with different areas of focus (e.g., performance for wasm3, blockchain applications for eos-vm, small footprint for wasm-micro-runtime). 

- One challenge for these runtimes is to implement and experiment with the new batch of WebAssembly proposals that strive to fulfill WebAssembly’s vision outside the browser.

- Although Wasmtime is implemented in Rust, the developers maintain APIs for embedding it within various other languages: C, Python, Go & .NET

# <img height="48" src="https://raw.githubusercontent.com/wasmerio/wasmer/master/assets/logo.png" alt="Wasmer logo" valign="middle"> Wasmer Python [![PyPI version](https://img.shields.io/pypi/v/wasmer)](https://badge.fury.io/py/wasmer) [![Wasmer Python Documentation](https://img.shields.io/badge/docs-read-green)](https://wasmerio.github.io/wasmer-python/api/wasmer/) [![Wasmer PyPI downloads](https://pepy.tech/badge/wasmer)](https://pypi.org/project/wasmer/) [![Wasmer Slack Channel](https://img.shields.io/static/v1?label=chat&message=on%20Slack&color=green)](https://slack.wasmer.io)

A complete and mature WebAssembly runtime for Python based on
[Wasmer](https://github.com/wasmerio/wasmer).

Features:

  * **Easy to use**: The `wasmer` API mimics the standard WebAssembly API,
  * **Fast**: `wasmer` executes the WebAssembly modules as fast as
    possible, close to **native speed**,
  * **Safe**: All calls to WebAssembly will be fast, but more
    importantly, completely safe and sandboxed,
  * **Modular**: `wasmer` can compile the WebAssembly modules with
    different engines or compiler.

**Documentation**: [browse the detailed API
documentation](https://wasmerio.github.io/wasmer-python/api/wasmer/) full of
examples.

**Examples** as tutorials: [browse the `examples/`
directory](https://github.com/wasmerio/wasmer-python/tree/master/examples),
it's the best place for a complete introduction!