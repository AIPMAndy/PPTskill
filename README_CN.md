# PPTskill — AI 驱动的 PPTX 生成工具（优化分支）

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![基于 ppt-master](https://img.shields.io/badge/基于-ppt--master-blue)](https://github.com/hugohe3/ppt-master)

[English](./README.md) | 中文

**PPTskill** 是 [`hugohe3/ppt-master`](https://github.com/hugohe3/ppt-master) 的优化分支，专注于实际工作流集成和 OpenClaw 兼容性。

输入 PDF、DOCX、URL 或 Markdown — 输出**原生可编辑的 PowerPoint**，包含真实的形状、文本框和图表。不是图片。点击任何元素都可以直接编辑。

## 与上游项目的区别

本分支新增：

- ✅ **OpenClaw skill 集成** — 无缝融入 OpenClaw 工作流
- ✅ **简化的安装流程** — 更清晰的依赖管理
- ✅ **工作流文档** — 真实项目的实用使用模式
- ✅ **已验证示例** — 在 macOS/Linux 上验证过的工作路径

所有核心 PPT 生成能力来自优秀的上游项目。本分支专注于让它在生产工作流中更易用。

## 快速开始

### 1. 安装

**必需：** [Python](https://www.python.org/downloads/) 3.8+  
**可选：** [Node.js](https://nodejs.org/) 18+（用于微信文章转换）· [Pandoc](https://pandoc.org/)（用于 DOCX/EPUB 转换）

```bash
# macOS
brew install python
brew install node                # 可选
brew install pandoc              # 可选

# Ubuntu/Debian
sudo apt install python3 python3-pip
sudo apt install nodejs npm      # 可选
sudo apt install pandoc          # 可选
```

```bash
git clone https://github.com/AIPMAndy/PPTskill.git
cd PPTskill
pip install -r requirements.txt
```

### 2. 选择 AI 编辑器

| 工具 | 评分 | 说明 |
|------|:------:|-------|
| **[Claude Code](https://claude.ai/)** | ⭐⭐⭐ | 最佳效果 — 原生 Opus，最大上下文 |
| [Cursor](https://cursor.sh/) / [VS Code + Copilot](https://code.visualstudio.com/) | ⭐⭐ | 不错的替代方案 |
| **[OpenClaw](https://openclaw.ai/)** | ⭐⭐⭐ | 推荐用于工作流自动化 |

### 3. 创建

打开 AI 对话面板，描述你想要的内容：

```
你：我有一份 Q3 季度报告需要做成 PPT

AI：好的。让我们确认设计规格：
    [模板] B) 无模板
    [格式] PPT 16:9
    [页数] 8-10 页
    ...
```

AI 会处理一切 — 内容分析、视觉设计、SVG 生成和 PPTX 导出。

> **输出：** `.pptx` 文件包含原生形状 — 可直接编辑。同时会生成一个 `_svg.pptx` 参考文件（在 PowerPoint 中使用"转换为形状"来编辑）。需要 Office 2016+。

### 4. 从现有项目导出

如果你已经有一个包含 `svg_final/` 目录的项目：

```bash
python3 skills/ppt-master/scripts/svg_to_pptx.py <项目路径> -s final
```

示例：

```bash
python3 skills/ppt-master/scripts/svg_to_pptx.py examples/ppt169_顶级咨询风_构建有效AI代理_Anthropic -s final
```

## 示例库

查看 [`examples/`](./examples/) — 15 个项目，229 页已验证的工作示例。

## OpenClaw 集成

如果你在使用 OpenClaw，本仓库在 `skills/PPTskill/SKILL.md` 包含了 skill 定义。

使用方法：

1. 将本仓库克隆到你的 OpenClaw 工作区
2. skill 会被自动检测
3. 询问你的 agent："从这个文档生成一个 PPT"

## 已知限制

- 在某些系统上，完整依赖安装可能因 `pycairo` / `cairo` 要求而失败
- 这**不会**阻塞核心 PPT 导出功能
- DOCX/EPUB 转换需要 `pandoc`（可选）

## 已验证的工作路径

测试环境：

- macOS（Apple Silicon + Intel）
- Python 3.11
- 上游 commit：`e0d2208`

核心导出路径确认可用：

- ✅ `svg_final/` → 可编辑 `.pptx`
- ✅ 原生 PPTX 生成
- ✅ 示例项目成功导出

## 设计哲学

遵循实用工程原则：

1. **首先验证最短工作路径**
2. **删除不必要的复杂性**
3. **稳定工作流**
4. **只在证明有价值后才自动化**

## 上游致谢

所有主要 PPT 生成能力来自：

- **[hugohe3/ppt-master](https://github.com/hugohe3/ppt-master)**

本分支的存在是为了让这个优秀的工作更容易集成到真实工作流中。

## 贡献

欢迎贡献！请：

- 保持改动专注于工作流改进
- 记录你测试过的内容
- 尊重上游项目的设计决策

## 许可证

MIT License（与上游相同）

本仓库包含工作流文档和集成改进。
请尊重上游仓库的许可证和署名要求。

## 链接

- **上游项目：** https://github.com/hugohe3/ppt-master
- **本分支：** https://github.com/AIPMAndy/PPTskill
- **OpenClaw：** https://openclaw.ai/
