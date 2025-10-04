# Waterloo Softare Distribution Kernel Networking Source

This directory contains the source files that make up networking functionalities for the Waterloo Software Distribution kernel.

## Source Roadmap

| Directory | Description |
| --------- | ----------- |
| core | core networking code |
| net80211 | wireless networking (IEEE 802.11) - `net80211(4)` |
| netgraph | graph-based networking subsystem - `netgraph(4)` |
| inet | IPv4 protocol implementation - `inet(4)` |
| inet6 | IPv6 protocol implementation - `inet6(4)` |
| ipsec | IPsec protocol implementation - `ipsec(4)` |
| pfil | packet filters - `ipfw(4)`, `pf(4)`, and `ipfilter(4)` |
| tests | kernel networking unit tests |
