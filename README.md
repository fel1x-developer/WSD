# Waterloo Software Distribution

## Overview

Waterloo Software Distribution (WSD) is a hobby operating system inspired by BSD and FreeBSD.
The goal of this operating system is to implement UNIX-like operating system by *imitating* FreeBSD operating system.
It is mainly written in Zig to ensure type and memory safety.
This is a research project and currently there is no plan to grow this project as an alternative operating system to FreeBSD, Linux, macOS, Windows, or whatever.

## License

WSD follows BSD 2-clause license (sometimes referred as "Simplified BSD License" or "FreeBSD License"). Code licensed under other licenses should not be introduced in this project. Zig and assembly files should include SPDX license identifier as well as the full BSD 2-clause license text at the top of files.

## Features

- Complete operating system from bootloader to basic userland software.
- Compatible with latest version of Single Unix Specification (includes POSIX) and C standard.
- Follows Executable and Linkable Format (ELF) for code execution
- Majority of code is written in Zig with minimum code written in Assembly.
- No LLM use for code generation. LLM is still used for research and identifying issues.
- No third party library except for Zig standard library, licensed under MIT license.

## Standard

When there is a conflict between POSIX, FreeBSD, and other standards, we follow the priority list below.

1. Latest release of Single Unix Specification and POSIX
2. Historical release of Single Unix Specification and POSIX
3. Latest release of C language standard
4. Historical release of C language standard
5. Any interface documented in FreeBSD man page
6. New features including experimental APIs for research purpose

## Platform

Inspired by FreeBSD's [platform targets](https://docs.freebsd.org/en/articles/committers-guide/#_platform_targets) system, platforms are devided into four tiers.

1. Tier 1 (riscv64): Main target on WSD. Development is mainly focused on these platforms. All bugs should be fixed. Tests should be provided for these platforms.

2. Tier 2 (amd64, arm64): Experimental target on WSD. Usually development isn't focused on these platforms, but developers should consider future implementation on them. All bugs should be fixed. Tests should be provided for these platforms.

3. Tier 3 (powerpc64): No support. Issues on these platforms does not hinder development process. Bug fixes is not prioritized and no tests are provided.

3. Tier 4 (VAX, PDP-11, MIPS, Alpha): Code for these platforms should never be introduced.
