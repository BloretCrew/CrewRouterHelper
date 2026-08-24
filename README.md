# CrewRouterHelper

CrewRouter 客户端事件统一上报工具 —— 让任何 AI 客户端（Claude Code / Codex /
Grok / OpenCode / Qwen Code / Hermes / OpenClaw / DeepSeek Harness）把本地
会话与工具调用事件上报到 CrewRouter 实时活动看板。

## Node.js 版（推荐）

零第三方依赖 CLI，npm 发布名 `@bloret/crewrouter-helper`：

```bash
npm i -g @bloret/crewrouter-helper
crewrouter-helper login          # 浏览器 OAuth 授权
crewrouter-helper test           # 验证链路
```

详见 [README.md](./README.md)（含各客户端 hooks 配置片段）。

## Python 参考版

`python-reference/` 内是功能一一对应的 Python 实现（标准库单文件，零依赖），
适合无 Node 环境的机器直接拷贝使用；`cr-login` 为 OAuth 凭证脚本，
`codex-cr` 为 Codex 启动包装。配置文件：`~/.config/cr-report.json`。

## 服务端要求

CrewRouter 主站（v1.0+，含 `/api/client-events` 与 OAuth 端点）。
