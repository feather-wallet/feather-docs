---
title: Supported Operating Systems
nav_title: Supported Operating Systems
category: installation
weight: 1000
---

Official Feather builds run on the following operating systems:

| Operating System | Minimum version                                           | Architecture               | 
|------------------|-----------------------------------------------------------|----------------------------|
| Linux            | [glibc 2.31](https://repology.org/project/glibc/versions) | x64, arm32, arm64, riscv64 |
| Windows          | [10 and higher](https://endoflife.date/windows)           | x64                        |
| macOS            | [12 and higher](https://endoflife.date/macos)             | Intel, Apple Silicon       |

It is strongly recommended that you run the latest version of Feather on an updated and supported operating system from 
a vendor you trust.
We try to support all major operating systems that are still supported by their respective vendors. 

If an operating system / distribution no longer receives security updates, we may drop support for it at any time. 
This allows us to keep our build system and dependencies up-to-date and ensures our releases benefit from optimizations 
and security improvements that modern compilers provide.

Using Feather on an unsupported ("End-of-Life") distribution increases the risk of malware infection due to unpatched security vulnerabilities which may result in a loss of privacy or a loss of funds.

#### Why no support for Windows 7 / 8.1 ?

Feather releases are built using the latest version of Qt, which dropped support for these operating systems.

Windows 7 and 8.1 stopped receiving security updates since January 2020 and January 2023, respectively.
We highly recommend that you update your machine to a newer version of Windows, or switch to a Linux distribution.
