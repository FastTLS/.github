# FastTLS

**Configurable network clients for Go, Python and Node.js.**

[Documentation](https://fasttls.github.io/) · [中文](README.md)

## Choose a client

- [Fastls for Go](https://github.com/FastTLS/fastls): stable core v0.1.1; TLS/HTTP profiles, JA3/JA4R, complete Spec, sessions, streaming and proxies.
- [Python SDK](https://github.com/FastTLS/fastls-ffi): `pip install --only-binary=:all: fastls==0.1.3`; synchronous and asyncio APIs with bundled native libraries.
- [Node.js SDK](https://github.com/FastTLS/fastls-ffi/tree/main/node): `npm install @fastls/fastls@0.10.1-dev.0`; Promise APIs, TypeScript and ESM/CommonJS. This is a development version.

[Getting started](https://fasttls.github.io/guide/) · [Capabilities and limits](https://fasttls.github.io/concepts/support) · [Troubleshooting](https://fasttls.github.io/help/). Documentation currently uses Chinese as its primary language.

## Ecosystem

[imitate](https://github.com/FastTLS/imitate) generates profiles; [ftransport](https://github.com/FastTLS/ftransport) implements configurable H1/H2 transport using standard net/http types; [profile](https://github.com/FastTLS/fastls/tree/v2/profile) defines the shared schema.

[Fetch](https://github.com/FastTLS/fastls-fetch), [RPC](https://github.com/FastTLS/fastls-rpc), [MITM](https://github.com/FastTLS/fastls-mitm), and [fastls-lab](https://github.com/FastTLS/fastls-lab) provide request services, authorized debugging and limited independent protocol observations. [fastls-fingerprints](https://github.com/FastTLS/fastls-fingerprints) has no formally released dataset. Historical fhttp/oohttp and protocol forks are not necessarily current core dependencies.

## Scope, licensing and responsibility

A profile name, User-Agent or successful request does not establish full equivalence with a real browser. Consult each tool for H3, WS, platform and runtime limits. Use only authorized systems and protect credentials and captured data. No anonymity or third-party acceptance is guaranteed.

Most FastTLS-owned core/SDK code uses Apache-2.0; third-party and historical repositories retain their actual terms. The upstream authorization gap for fhttp additions remains unresolved and must not be presented as blanket BSD/Apache permission. See the [licensing and disclaimer guide](https://fasttls.github.io/legal).

Report sanitized reproductions in the relevant repository. See [Contributing](https://github.com/FastTLS/.github/blob/main/CONTRIBUTING.md) and [Security](https://github.com/FastTLS/.github/blob/main/SECURITY.md).
