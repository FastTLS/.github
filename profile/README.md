<div align="center">

# FastTLS

**面向 Go 的 TLS 指纹与 HTTP 请求工具集**

生成配置 · 发送请求 · 独立观测

[核心库](https://github.com/FastTLS/fastls) · [指纹生成器](https://github.com/FastTLS/imitate) · [English](https://github.com/FastTLS/.github/blob/main/profile/README_EN.md)

</div>

FastTLS 围绕 TLS ClientHello、HTTP 协议参数与请求头顺序，提供可组合的请求库、指纹生成器、跨语言接口和诊断工具，服务于客户端兼容性测试、协议研究与请求行为调试。

## 从这里开始

- **在 Go 中发送请求** → [fastls](https://github.com/FastTLS/fastls)：支持自定义 JA3 / JA4R、完整 `profile.Spec`、请求头顺序以及 HTTP / HTTPS / SOCKS5 代理。
- **生成或导出指纹配置** → [imitate](https://github.com/FastTLS/imitate)：独立生成 browser、library 和 client 配置；通过 Provider 接入请求库，也可导出离线 Bundle。
- **通过 Python 或 C ABI 接入** → [fastls-ffi](https://github.com/FastTLS/fastls-ffi)：提供动态库和 Python SDK，包含同步、异步及流式响应接口，当前处于早期开发阶段。
- **观测实际发送的参数** → [fastls-lab](https://github.com/FastTLS/fastls-lab)：独立采集 TLS、HTTP/1、HTTP/2 及 WS/WSS 的部分协议行为，用于诊断与验证。

## 项目生态

### 配置与证据

- [fastls/profile](https://github.com/FastTLS/fastls/tree/v2/profile)：请求库与生成器共享的配置规范。
- [fastls-fingerprints](https://github.com/FastTLS/fastls-fingerprints)：指纹证据、覆盖记录与固定导出数据；可执行生成规则维护在 imitate。

### 服务与集成

- [fastls-fetch](https://github.com/FastTLS/fastls-fetch)：HTTP Fetch 服务。
- [fastls-rpc](https://github.com/FastTLS/fastls-rpc)：JSON-RPC 与 gRPC 接口。
- [fastls-mitm](https://github.com/FastTLS/fastls-mitm)：用于测试和调试的 MITM 代理。

服务的可用接口、构建方式及依赖版本以各仓库说明为准。

### 协议依赖

组织内维护 [fhttp](https://github.com/FastTLS/fhttp)、[utls](https://github.com/FastTLS/utls)、[quic-go](https://github.com/FastTLS/quic-go) 和 [oohttp](https://github.com/FastTLS/oohttp) 等协议相关仓库。各项目的来源、授权和使用方式请查看对应仓库；组织内存在某个 fork 不代表核心库当前依赖该 fork。

## 开发状态与能力范围

当前 Fastls v2 与 imitate v2 处于开发候选阶段，尚未作为正式 Go 模块版本发布。开始集成前，请阅读目标分支的 README、[核心开发说明](https://github.com/FastTLS/fastls/blob/v2/DEVELOPMENT.md)及[发布前置条件](https://github.com/FastTLS/fastls/blob/v2/RELEASE.md)，并固定所用版本或提交。

浏览器名称、版本身份和 User-Agent 不等于真实浏览器全部协议行为已经验证。配置范围以 Provider 的 `List`、解析结果 `Match` 和对应证据为准；完整 Spec 当前支持 HTTP/1 与 HTTP/2，HTTP/3 等能力边界请查看[指纹接入说明](https://github.com/FastTLS/fastls/blob/v2/imitate/README.md)。

## 参与贡献

欢迎改进文档、提交最小复现、补充协议测试和可追溯的指纹证据。请在对应项目中提交 Issue 或 Pull Request；组织首页和公共模板的问题在 [此仓库](https://github.com/FastTLS/.github/issues)反馈。

阅读[贡献指南](https://github.com/FastTLS/.github/blob/main/CONTRIBUTING.md)。各仓库的许可证及上游声明以其自身文件为准。
