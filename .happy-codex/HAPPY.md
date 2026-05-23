# Happy-Codex Marketplace

## 项目概述

happy-codex 插件市场仓库，用于存放和分发 happy-codex 插件。

## 插件列表

| 插件 | 说明 |
|------|------|
| **andrej-karpathy-skills** | 受 Andrej Karpathy 启发的编码准则，帮助减少 LLM 常见编码错误 |

## 目录结构

```
./
├── .happy-codex/              # Happy-Codex 配置
├── andrej-karpathy-skills/   # 插件目录
│   ├── plugin.json           # 插件清单
│   ├── README.md             # 英文文档
│   ├── README.zh.md          # 中文文档
│   ├── CLAUDE.md             # Claude Code 指南
│   ├── skills/               # Skill 定义
│   │   └── karpathy-guidelines/
│   │       ├── SKILL.md      # Skill 配置
│   │       └── README.zh.md # 中文说明
│   ├── commands/             # 命令目录（可扩展）
│   ├── agents/               # 代理目录（可扩展）
│   ├── hooks/                # 钩子目录（可扩展）
│   └── .cursor/
│       └── rules/            # Cursor 规则
│           └── karpathy-guidelines.mdc
```

## 插件开发规范

### 创建新插件

```bash
mkdir my-plugin
cd my-plugin
mkdir -p skills/commands/agents/hooks
```

### 插件清单 (plugin.json)

```json
{
  "name": "my-plugin",
  "version": "1.0.0",
  "description": "插件描述",
  "skills": ["./skills/my-skill"],
  "commands": [],
  "agents": [],
  "hooks": {}
}
```

### Skill 定义 (skills/*/SKILL.md)

```markdown
---
name: my-skill
description: 简短描述
allowed-tools: [read_file, write_to_file]
context: inline
when-to-use: 使用场景描述
user-invocable: true
---

# Skill 内容
```

## 架构要点

- **Skill**: 可复用的提示模板，通过 `when-to-use` 自动触发或手动 `/skill-name` 调用
- **Command**: 自定义斜杠命令，支持 prompt 或 local 模式
- **Agent**: 子代理定义，可并行处理复杂任务
- **Hook**: 生命周期钩子，在工具执行前后注入逻辑
- **plugin.json**: 唯一必需文件，定义插件元数据和功能入口

## 已知问题

- 暂无

## 添加新插件

1. 在根目录创建插件文件夹
2. 按规范编写 `plugin.json`
3. 添加 `skills/`、`commands/`、`agents/` 或 `hooks/` 目录
4. 在对应目录添加功能文件