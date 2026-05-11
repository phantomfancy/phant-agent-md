# phant-agent-md

![Stars](https://img.shields.io/github/stars/phantomfancy/phant-agent-md?style=social)
![Language](https://img.shields.io/badge/language-Markdown-blue)
![Purpose](https://img.shields.io/badge/purpose-Agent%20Instructions-2ea44f)
![License](https://img.shields.io/badge/license-MIT-yellow)

这是我为编码代理编写的全局指令文件。

My global instruction file for LLM coding agents.

## 使用方式

直接使用AGENT.md文件即可。

对 Claude Code, Codex, OpenCode等支持全局AGENT.md的工具：复制到工具的config目录即可；

对 Cursor 或 Windsurf等只支持项目级别AGENT.md的工具：单独复制到项目根目录。

## Usage

Just use AGENT.md file directly, and it's done.

For tools that supports global AGENT.md like Claude Code, Codex, OpenCode: copy AGENT.md to your tool's config directory.

For tools that only supports project-level AGENT.md like Cursor of Windsurf: add the file to each repo manually.
