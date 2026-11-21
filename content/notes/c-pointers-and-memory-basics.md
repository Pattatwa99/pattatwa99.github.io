---
title: "C Pointers & Memory Layout Basics"
date: 2026-11-15
tags: ["C", "Memory", "Pointers"]
summary: "Concise reference on pointers, dereferencing, and memory addresses in C."
---

A quick reference on pointer basics and memory mechanics in C:

### Declaration & Operators

- `int *ptr`: Declares `ptr` as a pointer to an integer.
- `&var`: Address-of operator, yields the memory address of `var`.
- `*ptr`: Dereference operator, accesses or modifies the value located at `ptr`.

```c
int val = 42;
int *p = &val;

printf("Value: %d\n", *p);      // Prints 42
printf("Address: %p\n", (void*)p); // Memory address

*p = 100; // Modifies val via pointer dereference
```

### Key Reminders

- Always initialize pointers (`NULL` or a valid address) before dereferencing.
- Array names decay into pointers to their first element when passed into functions.
- `sizeof(ptr)` gives the pointer's size (usually 8 bytes on x86_64), not the pointed buffer's size.
