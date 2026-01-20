# XINU Operating Systems Projects

This repository serves as an index for three operating systems projects implementing core kernel subsystems in the XINU educational operating system. Each project addresses fundamental challenges in OS design: process scheduling, virtual memory management, and file system optimization.

## Projects

### Process Scheduling

Implementation of two CPU scheduling algorithms to address starvation in priority-based scheduling. The **Exponential Distribution Scheduler** uses probabilistic selection based on exponential distribution (λ=0.1) to balance priority with fairness. The **Linux-like Scheduler** emulates the Linux 2.2 kernel scheduler with epoch-based quantum allocation, dynamic goodness calculation, and quantum carryover mechanisms.

**Repository:** [xinu-scheduler](https://github.com/devangsaraogi/xinu-scheduler)

### Virtual Memory System

Full implementation of demand paging with virtual memory support. Features include multi-level page tables (page directories and page tables), page fault handling via interrupt 14, eight backing stores emulating swap space, and the Second-Chance page replacement algorithm. Implements system calls for memory mapping (`xmmap`, `xmunmap`), virtual process creation (`vcreate`), and virtual heap management (`vgetmem`, `vfreemem`).

**Repository:** [xinu-virtual-memory](https://github.com/devangsaraogi/xinu-virtual-memory)

### File System Defragmenter

Disk defragmentation utility for Unix-style file systems. Reorganizes fragmented files by relocating data blocks to contiguous regions on disk, reconstructs multi-level indirect block hierarchies (direct, single, double, and triple indirect), and optimizes free block lists to prevent future fragmentation. Handles variable block sizes and preserves inode metadata.

**Repository:** [xinu-filesystem-defragmenter](https://github.com/devangsaraogi/xinu-filesystem-defragmenter)

## Technologies & Concepts

**Languages:** C, x86 Assembly (AT&T syntax)

**Core Concepts:** Process scheduling algorithms, context switching, virtual memory management, demand paging, page replacement policies, TLB management, interrupt handling, file system structures, inode management, block allocation

**Architecture:** Intel x86 (32-bit), multi-level page tables, inverted page tables, backing store management

**Tools:** GCC toolchain, GNU Assembler, GDB, QEMU emulator, GNU Make

## Source Code Availability

Complete implementations are maintained in the linked repositories. Each repository contains detailed documentation, build instructions, and technical specifications. Access is publicly available for portfolio review.

## Acknowledgments

These projects were completed as part of **CSC 501: Operating Systems Principles** at North Carolina State University (Fall 2025), instructed by **Prof. Man-Ki Yoon**. The course provides hands-on experience with operating system internals through the XINU educational operating system.
