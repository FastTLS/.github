# 贡献指南 / Contributing

欢迎提交文档改进、问题复现、协议测试和指纹证据。中文或英文均可；目标仓库若有自己的贡献指南，请优先遵循。

Contributions in Chinese or English are welcome. Follow the target repository's contribution guide when one is provided.

## 选择仓库 / Choose a repository

- 请求行为、指纹应用 / Request behavior and profile application: [fastls](https://github.com/FastTLS/fastls)
- 配置生成、规范 ID 解析 / Profile generation and canonical ID resolution: [imitate](https://github.com/FastTLS/imitate)
- 固定数据与证据 / Fixed data and evidence: [fastls-fingerprints](https://github.com/FastTLS/fastls-fingerprints)
- 采集器与观测 / Collectors and observations: [fastls-lab](https://github.com/FastTLS/fastls-lab)
- C ABI、Python SDK / Language bindings: [fastls-ffi](https://github.com/FastTLS/fastls-ffi)
- 服务接口 / Service interfaces: 对应的 Fetch、RPC 或 MITM 仓库 / the relevant Fetch, RPC, or MITM repository
- 组织首页与公共模板 / Organization profile and shared templates: [.github](https://github.com/FastTLS/.github)

## 报告问题 / Report a bug

先搜索已有 Issue。提供分支或提交 SHA、运行环境、最小复现、预期行为与实际结果。涉及指纹时，补充规范 ID、自定义 JA3 / JA4R 或 Spec、解析策略及脱敏观测；区分生成配置、网络观测和真实浏览器参考样本。

Search existing issues first. Include the branch or commit SHA, environment, minimal reproduction, expected behavior, and actual result. For fingerprint issues, include the canonical ID or custom JA3 / JA4R or Spec, resolution policy, and sanitized observations. Distinguish generated configurations, wire observations, and real browser reference samples.

分享日志或抓包前移除 Token、Cookie、代理凭据和私有目标地址。

Remove tokens, cookies, proxy credentials, and private target addresses from shared logs and captures.

## 提交修改 / Submit a change

1. 从目标仓库的相应分支创建工作分支；先阅读该分支的开发说明。当前开发分支和已发布版本可能不同。
2. 围绕一个明确问题修改；跨仓改动注明依赖仓库和提交。
3. 按仓库说明完成相关检查；行为修复尽量包含能复现问题的测试。纯文档修改检查链接、示例和中英文一致性。
4. 在 PR 中解释问题、修改后的行为、验证结果和已知限制。未运行的检查请注明原因。

1. Branch from the appropriate target branch and read its development instructions. Development APIs may differ from released versions.
2. Keep the change focused. Identify dependent repositories and commits for cross-repository changes.
3. Run the relevant repository checks. Include a reproducing test for behavior fixes where practical. For documentation changes, check links, examples, and language consistency.
4. Describe the problem, resulting behavior, validation, and known limitations in the PR. Explain any checks you could not run.

## 指纹数据 / Fingerprint data

提供来源、采集方法、浏览器或客户端版本、操作系统及原始观测与处理方法。仅有 UA、配置生成成功或请求成功不足以证明指纹一致。提交生成物时记录生成器修订和复现步骤，并遵循目标仓库的数据维护方式。

Include provenance, collection method, browser or client version, OS, raw observations, and processing steps. A User-Agent, successful profile generation, or a successful request alone does not prove fingerprint equivalence. Record the generator revision and reproduction steps for generated artifacts, following the target repository's data workflow.

提交前检查目标仓库的许可证和上游声明，确保有权贡献相关代码、数据或素材。

Check the target repository's license and upstream notices, and ensure you have permission to contribute the code, data, or assets.
