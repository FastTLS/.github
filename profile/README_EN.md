<div align="center">

# FastTLS

**TLS fingerprinting and HTTP request tools for Go**

Generate profiles · Send requests · Observe protocol behavior

[Core library](https://github.com/FastTLS/fastls) · [Profile generator](https://github.com/FastTLS/imitate) · [中文](https://github.com/FastTLS/.github/blob/main/profile/README.md)

</div>

FastTLS provides composable request libraries, profile generation, language bindings, and diagnostic tools for TLS ClientHello parameters, HTTP protocol settings, and header ordering. These projects support client compatibility testing, protocol research, and request debugging.

## Start here

- **Send requests from Go** → [fastls](https://github.com/FastTLS/fastls): custom JA3 / JA4R, complete `profile.Spec` configurations, header ordering, and HTTP / HTTPS / SOCKS5 proxies.
- **Generate or export profiles** → [imitate](https://github.com/FastTLS/imitate): an independent generator for browser, library, and client profiles. Integrate through a Provider or export an offline Bundle.
- **Integrate through Python or a C ABI** → [fastls-ffi](https://github.com/FastTLS/fastls-ffi): a shared library and Python SDK with synchronous, asynchronous, and streaming response interfaces. Currently in early development.
- **Inspect what was actually sent** → [fastls-lab](https://github.com/FastTLS/fastls-lab): independent observation of selected TLS, HTTP/1, HTTP/2, and WS/WSS behaviors for diagnosis and verification.

## Ecosystem

### Profiles and evidence

- [fastls/profile](https://github.com/FastTLS/fastls/tree/v2/profile): the shared profile specification for the request library and generators.
- [fastls-fingerprints](https://github.com/FastTLS/fastls-fingerprints): evidence, coverage records, and fixed data exports. Executable generation rules are maintained in imitate.

### Services and integrations

- [fastls-fetch](https://github.com/FastTLS/fastls-fetch): an HTTP Fetch service.
- [fastls-rpc](https://github.com/FastTLS/fastls-rpc): JSON-RPC and gRPC interfaces.
- [fastls-mitm](https://github.com/FastTLS/fastls-mitm): a MITM proxy for testing and debugging.

Consult each repository for available interfaces, build instructions, and dependency versions.

### Protocol dependencies

The organization hosts protocol repositories including [fhttp](https://github.com/FastTLS/fhttp), [utls](https://github.com/FastTLS/utls), [quic-go](https://github.com/FastTLS/quic-go), and [oohttp](https://github.com/FastTLS/oohttp). Check each repository for provenance, licensing, and usage. Hosting a fork does not imply that the core library currently depends on it.

## Development status and scope

Fastls v2 and imitate v2 are development candidates and have not been published as formal Go module releases. Before integrating, read the target branch's README, the [core development guide](https://github.com/FastTLS/fastls/blob/v2/DEVELOPMENT.md), and the [release prerequisites](https://github.com/FastTLS/fastls/blob/v2/RELEASE.md). Pin the version or commit you use.

A browser name, version identity, or User-Agent does not establish full protocol equivalence with a real browser. Consult the Provider's `List`, the resolved `Match`, and supporting evidence. Complete Spec configurations currently support HTTP/1 and HTTP/2; see the [integration guide](https://github.com/FastTLS/fastls/blob/v2/imitate/README.md) for HTTP/3 and other capability boundaries.

## Contribute

Documentation improvements, minimal reproductions, protocol tests, and traceable fingerprint evidence are welcome. Open an Issue or Pull Request in the relevant project. Report organization profile and shared template issues in [this repository](https://github.com/FastTLS/.github/issues).

Read the [contribution guide](https://github.com/FastTLS/.github/blob/main/CONTRIBUTING.md). Licensing and upstream notices are defined by each repository's own files.
