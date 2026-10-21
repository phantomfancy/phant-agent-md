# phant-agent-md

![Stars](https://img.shields.io/github/stars/phantomfancy/phant-agent-md?style=social)
![Language](https://img.shields.io/badge/language-Markdown-blue)
![Purpose](https://img.shields.io/badge/purpose-Agent%20Instructions-2ea44f)
![License](https://img.shields.io/badge/license-MIT-yellow)

这是我为编码代理编写的全局指令文件。

My global instruction file for LLM coding agents.

## 使用方式

使用本仓库的 `AGENTS.md` 作为指令模板。

对于 Codex，将文件内容合并到 `~/.codex/AGENTS.md` 作为全局默认指令，或合并到项目根目录的 `AGENTS.md` 作为项目指令。若设置了 `CODEX_HOME`，全局文件应放在该目录。保留已有指令，并处理冲突；具体加载与覆盖规则见 [Codex 官方文档](https://learn.chatgpt.com/docs/agent-configuration/agents-md)。

其他工具请按各自文档配置指令文件名和位置，不要假定它们采用相同的加载规则。

## Usage

Use this repository's `AGENTS.md` as an instruction template.

For Codex, merge the contents into `~/.codex/AGENTS.md` for global defaults or into `AGENTS.md` at the project root for project instructions. If `CODEX_HOME` is set, place the global file in that directory. Preserve existing instructions and resolve conflicts. See the [Codex documentation](https://learn.chatgpt.com/docs/agent-configuration/agents-md) for discovery and override rules.

For other tools, follow their documentation for instruction filenames and locations; do not assume they use the same discovery rules.
