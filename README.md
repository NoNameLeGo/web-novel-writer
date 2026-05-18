# Web Novel Writer — AI 网文写作工作流

一个为 AI 辅助长篇网络小说创作设计的结构化工作流 skill。适用于 OpenCode / Claude Code 等支持 skill 机制的 AI 编程助手。

## 概览

这不是一个"你写一句 AI 补一句"的聊天工具，而是一套**导演式生产管线**：

```
灵感 → 题材定位 → 世界观搭建 → 人物设定 → 大纲规划 →
风格定义 → 章节生成 → 一致性检查 → 去AI味优化 → 导出
```

## 核心功能

- **完整创作管线**：从灵感脑暴到最终章节导出的 10 步流程
- **结构化 Prompt 体系**：章纲生成、正文生成、续写扩写、风格微调等 13+ 场景化模板
- **多 API 支持**：OpenAI / Claude / DeepSeek / OpenRouter / Ollama / 任意兼容端点
- **写法引擎**：可定义和切换写作风格（轻松日常 / 热血战斗 / 悬疑推理等）
- **一致性检查**：角色、设定、情节、文风的四维自动校验
- **去 AI 味优化**：专有检查清单消除 AI 生成痕迹
- **网文节奏引擎**：爽点密度、钩子强度、章节节奏的动态控制

## 文件结构

```
web-novel-writer/
├── SKILL.md                   # 主 skill 文件 — 完整工作流定义
├── LICENSE                    # GPL-3.0 协议
├── README.md                  # 本文件
└── references/
    ├── prompts.md             # 全套可复用 Prompt 模板
    └── examples.md            # 实际输出示例展示
```

## 快速开始

### 方式一：在 OpenCode 中使用

1. 将 `web-novel-writer` 目录放入项目的 `.opencode/skills/` 目录
2. 重启 OpenCode，skill 会被自动发现
3. 对话中提到"写网文"或加载 skill 即可使用

### 方式二：作为独立 Prompt 参考

直接阅读 `SKILL.md` 和 `references/prompts.md` 中的模板，手动用于任何 AI 工具。

## 支持的 API/模型

| 提供商 | 配置方式 | 推荐模型 |
|--------|---------|---------|
| OpenAI | `OPENAI_API_KEY` | GPT-4o / GPT-4o-mini |
| Claude | `ANTHROPIC_API_KEY` | Claude Sonnet |
| DeepSeek | `DEEPSEEK_API_KEY` | DeepSeek-V3 / R1 |
| OpenRouter | `OPENROUTER_API_KEY` | 聚合多种模型 |
| Ollama (本地) | Ollama API | Qwen2.5 / Llama3 |

## 设计理念

本 skill 的设计参考了以下开源项目：

- [AI-Novel-Writing-Assistant](https://github.com/DLM1997/AI-Novel-Writing-Assistant) — AI 导演 / Agent Runtime / 世界观联动架构
- [writing-helper](https://github.com/ivone-liu/writing-helper) — 多 API 写作辅助 / 风格编辑 / AI 优化
- [AIStoryWriter](https://github.com/ymhyx/AIStoryWriter) — Ollama 集成 / 可配置生成管线
- [jacobbeasley/novelai](https://github.com/jacobbeasley/novelai) — 大纲 → 章节 → 导出完整管线

## License

[GNU General Public License v3.0](LICENSE)
