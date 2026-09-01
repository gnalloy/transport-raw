# Overview

[简体中文](overview.zh-CN.md) | [Docs Index](README.md)

## Purpose

Raw IP protocol transport for Gnalloy with packet messages and explicit privileged runtime boundaries.

This module owns an I/O boundary. It creates or adapts Gnalloy Channels for a concrete transport while protocol parsing, business handlers, TLS policy, and observability remain in other modules.

## Repository Identity

- Module path: `gnalloy.org/transport-raw`
- GitHub repository: `github.com/gnalloy/transport-raw`
- Default branch: `dev`
- License: Apache-2.0

## Package Map
- `gnalloy.org/transport-raw` (`raw`)

## Direct Gnalloy Dependencies
- `gnalloy.org/gnalloy`

## Direct Dependents in the Current Module Plan
- `gnalloy.org/codec-icmp`
- `gnalloy.org/codec-ip`
- `gnalloy.org/examples`
- `gnalloy.org/handler-ipfilter`
- `gnalloy.org/handler-pcap`
- `gnalloy.org/protocol`

## Architecture Position

Gnalloy keeps the core small and dependency-light. This repository is a replaceable module around one responsibility, connected through explicit Go packages instead of runtime discovery.

## Compatibility

The public import path is `gnalloy.org/transport-raw`. Until the first stable tag is published, use `@dev` or an explicit pseudo-version selected by your dependency policy.
