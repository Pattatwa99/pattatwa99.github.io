---
title: "Notes on Systems Programming and the Linux Environment"
date: 2026-11-20
tags: ["C", "Linux", "Systems", "Fedora"]
summary: "Observations on working with C, compiler tooling, and systems programming on Fedora."
---

Systems programming provides a clear window into how operating systems and hardware actually function together. 

### Why Systems in C?

Writing code in C strips away high-level abstractions:
- Memory management is explicit.
- Data structures map directly to contiguous memory regions.
- System calls interface directly with the Linux kernel.

### The Linux Environment

Working primarily on Fedora, standard GNU toolchains (`gcc`, `gdb`, `make`, `valgrind`) provide powerful inspection tools. Being able to trace system calls with `strace` or inspect memory layouts demystifies what happens between application code and the processor.
