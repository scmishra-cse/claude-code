# Claude Code — Leaked Source

**The full source code of Anthropic's Claude Code CLI, leaked on March 31, 2026.**

[![TypeScript](https://img.shields.io/badge/TypeScript-512K%2B_lines-3178C6?logo=typescript&logoColor=white)](#tech-stack)
[![Bun](https://img.shields.io/badge/Runtime-Bun-f472b6?logo=bun&logoColor=white)](#tech-stack)
[![React + Ink](https://img.shields.io/badge/UI-React_%2B_Ink-61DAFB?logo=react&logoColor=black)](#tech-stack)
[![Files](https://img.shields.io/badge/~1,900_files-source_only-grey)](#directory-structure)
[![MCP Server](https://img.shields.io/badge/MCP-Explorer_Server-blueviolet)](#-explore-with-mcp-server)

---

## What is Claude Code?

Claude Code is Anthropic's official CLI tool for interacting with Claude directly from the terminal. It handles file editing, command execution, codebase searching, and git workflows. This repository contains the leaked `src/` directory for educational exploration.

| Property | Details |
|---|---|
| **Leaked** | 2026-03-31 |
| **Language** | TypeScript (strict) |
| **Runtime** | [Bun](https://bun.sh) |
| **Scale** | ~1,900 files · 512,000+ lines of code |

---

## 🔍 Explore with MCP Server

This repository includes an [MCP server](https://modelcontextprotocol.io/) that allows any MCP-compatible client (Claude Code, Claude Desktop, VS Code, Cursor) to explore the source code interactively.

### Quick Setup

```bash
# 1. Clone the repo
git clone https://github.com/scmishra-cse/claude-code.git
cd claude-code/mcp-server

# 2. Install & build
npm install && npm run build

# 3. Add to Claude Code
claude mcp add claude-code-explorer -- node $(pwd)/dist/index.js
```

### Key Tools
- `search_source`: Grep across the entire source tree.
- `read_source_file`: Read any file from `src/` by path.
- `list_tools` / `list_commands`: Explore the ~40 tools and ~50 commands available in Claude Code.

---

## Directory Structure

```
src/
├── main.tsx                 # CLI entrypoint (Commander + React/Ink)
├── QueryEngine.ts           # Core LLM API caller
├── tools/                   # Agent tool implementations (~40)
├── commands/                # Slash command implementations (~50)
├── services/                # External service integrations
├── bridge/                  # IDE integration (VS Code, JetBrains)
├── mcp/                     # Model Context Protocol implementation
└── components/              # Terminal UI components (Ink)
```

---

## Disclaimer

This repository archives source code leaked from Anthropic's npm registry on **2026-03-31**. All original source code is the property of [Anthropic](https://www.anthropic.com). This is not an official release and is not licensed for redistribution.
