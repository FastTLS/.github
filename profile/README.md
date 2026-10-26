# FastTLS

**精细控制 TLS 指纹与 HTTP 请求行为，支持 Go、Python 与 Node.js。**

[完整使用文档](https://fasttls.github.io/) · [English](README_EN.md)

## 选择你的工具

- **Go**：[fastls](https://github.com/FastTLS/fastls)，稳定核心 v0.1.1。TLS/HTTP 参数、JA3/JA4R、完整 Spec、连接池、流式与代理。
- **Python**：[fastls-ffi](https://github.com/FastTLS/fastls-ffi)，PyPI 安装 `fastls==0.1.4`。同步/asyncio，平台 wheel 内置动态库。
- **Node.js**：[fastls-ffi/node](https://github.com/FastTLS/fastls-ffi/tree/main/node)，npm 安装 `@fastls/fastls@0.10.1-dev.0`。Promise、TypeScript、ESM/CommonJS；当前是开发版本。

[快速开始](https://fasttls.github.io/guide/) · [支持与限制](https://fasttls.github.io/concepts/support) · [安装排错](https://fasttls.github.io/help/)

## 周边项目

[imitate](https://github.com/FastTLS/imitate) 生成配置；[ftransport](https://github.com/FastTLS/ftransport) 提供标准 net/http 类型的 H1/H2 传输；[fastls/profile](https://github.com/FastTLS/fastls/tree/v2/profile) 定义共享规范。

[Fetch](https://github.com/FastTLS/fastls-fetch) 提供 HTTP JSON 服务，[RPC](https://github.com/FastTLS/fastls-rpc) 提供 JSON-RPC/gRPC，[MITM](https://github.com/FastTLS/fastls-mitm) 用于授权代理调试，[fastls-lab](https://github.com/FastTLS/fastls-lab) 独立采集部分网络行为。[fastls-fingerprints](https://github.com/FastTLS/fastls-fingerprints) 尚无正式发布数据包。

历史 fhttp/oohttp 和协议派生仓库保留供追溯；它们的存在不等于当前核心依赖它们。

## 能力、协议与责任

配置名、UA 或一次成功请求不代表真实浏览器全部行为已经验证。H3、WS、系统平台及运行环境均有限制，以各工具文档和实际发布版本为准。只在授权范围内使用，保护凭据与捕获数据；不保证匿名性或第三方服务放行。

自有核心/SDK 主要采用 Apache-2.0，第三方与历史项目按实际许可证；fhttp 上游新增代码授权缺口仍未解决，不能统一认定为 Apache 或 BSD。完整声明见 [协议与免责声明](https://fasttls.github.io/legal)。

问题请到对应工具仓库提供脱敏最小复现。参与贡献阅读 [贡献指南](https://github.com/FastTLS/.github/blob/main/CONTRIBUTING.md)，敏感问题阅读 [安全报告](https://github.com/FastTLS/.github/blob/main/SECURITY.md)。
