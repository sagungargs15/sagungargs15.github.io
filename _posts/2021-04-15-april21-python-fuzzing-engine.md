---
layout: post
title: "April21-Python Fuzzing Engine: Atheris"
date: 2021-04-15 23:59:59 -0000
categories: automated-testing fuzzing-engine python vulnerability-research security-analysis
author: "Sagun Garg"
tags: automated-testing fuzzing-engine python vulnerability-research security-analysis
---

# Atheris....Whaaaa?

> Atheris can be used to automatically find bugs in Python code and native extensions. Atheris is a “coverage-guided” fuzzer, which means that Atheris will repeatedly try various inputs to your program while watching how it executes, and try to find interesting paths.

> Differential fuzzing and fuzz testing are powerful automated testing techniques that have found many bugs in existing software — C compilers, Java decompilers, antivirus software, and more. Nick Fitzgerald recently explained in an [InfoQ interview](https://www.infoq.com/articles/webassembly-wasmtime-tooling-reference-types/) how generative testing allows finding bugs that are not easy to detect with other methods

# Interesting Fact

> One of the best uses for Atheris is for differential fuzzers. These are fuzzers that look for differences in behavior of two libraries that are intended to do the same thing. One of the example fuzzers packaged with Atheris does exactly this to compare the Python “idna” package to the C “libidn2” package. Both of these packages are intended to decode and resolve internationalized domain names. However, the example fuzzer idna_uts46_fuzzer.py shows that they don’t always produce the same results. If you ever decided to purchase a domain containing (Unicode codepoints [U+0130, U+1df9]), you’d discover that the idna and libidn2 libraries resolve that domain to two completely different websites.

# Goal of Fuzzing ?
Fuzzing is useful to discover uncaught exceptions, and other API contract violations in Python. 

# What is Fuzzing ?
Fuzzing is a technique in computer testing and security where you generate a bunch of random inputs, and see how some program handles it. Fuzz testing is a well-known technique for uncovering programming errors. Many of these detectable errors have serious security implications.

# Fuzzing: Example python code

```
import atheris  
import sys  
  
def TestOneInput(data):  
if data == b"bad":  
raise RuntimeError("Badness!")  
  
atheris.Setup(sys.argv, TestOneInput)  
atheris.Fuzz()

```

# References
- [Google: Announcement of Open Source Release](https://opensource.googleblog.com/2020/12/announcing-atheris-python-fuzzer.html)
- [Intro to Fuzzing in Python](https://alexgaynor.net/2015/apr/13/introduction-to-fuzzing-in-python-with-afl/)
- [Google: Atheris Python Fuzzing](https://www.infoq.com/news/2021/01/google-python-atheris-fuzzing/)

# Learn References: Free
- [Introduction to Blackbox Fuzzing](https://academy.fuzzinglabs.com/introduction-blackbox-fuzzing)
- [Introduction to Python Fuzzing by Patrick Ventuzelo](https://academy.fuzzinglabs.com/introduction-python-fuzzing)

# # Follow the OGs
- Twitter [Patrick Ventuzelo](https://twitter.com/pat_ventuzelo)
- Github [Alex Gaynor](https://alexgaynor.net/)