<div align="center">

# 🎨 PPTskill

**AI 生成原生可编辑 PPTX — 无需设计技能，一键生成专业演示文稿**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Based on ppt-master](https://img.shields.io/badge/based%20on-ppt--master-blue)](https://github.com/hugohe3/ppt-master)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![OpenClaw Compatible](https://img.shields.io/badge/OpenClaw-compatible-green)](https://openclaw.ai/)

[English](./README_EN.md) | **简体中文**

<img src="docs/assets/screenshots/preview_magazine_garden.png" width="600" alt="PPTskill Demo">

</div>

---

## 🆚 为什么选 PPTskill？

| 能力 | 传统 PPT 工具 | 在线 AI PPT | **PPTskill** |
|------|:-------------:|:-----------:|:------------:|
| 原生可编辑 | ✅ | ❌ 图片/SVG | ✅ **真实形状** |
| AI 驱动 | ❌ | ✅ | ✅ |
| 本地运行 | ✅ | ❌ | ✅ **隐私安全** |
| 工作流集成 | ❌ | ❌ | ✅ **OpenClaw/Cursor** |
| 开源免费 | ❌ | ❌ | ✅ **MIT License** |
| 多种风格 | ⚠️ 需手动 | ⚠️ 有限 | ✅ **10+ 模板** |

**核心差异**：输出的是**真正的 PowerPoint 对象**（DrawingML），不是图片或 SVG 嵌入。点击任何元素都可以直接编辑。

---

## 🚀 30 秒快速开始

```bash
# 1. 克隆仓库
git clone https://github.com/AIPMAndy/PPTskill.git
cd PPTskill

# 2. 安装依赖
pip install -r requirements.txt

# 3. 导出示例 PPT
python3 skills/ppt-master/scripts/svg_to_pptx.py examples/ppt169_顶级咨询风_构建有效AI代理_Anthropic -s final

# ✅ 完成！在 examples/ 目录下找到生成的 .pptx 文件
```

**输出**：
- `项目名_时间戳.pptx` — 原生可编辑版本（推荐）
- `项目名_时间戳_svg.pptx` — SVG 参考版本

---

## 💡 核心功能

### 1️⃣ 多种输入格式

- 📄 **PDF** — 研究论文、报告
- 📝 **DOCX** — Word 文档
- 🌐 **URL** — 网页、博客文章
- 📋 **Markdown** — 技术文档

### 2️⃣ 10+ 专业模板

- 🏢 **顶级咨询风** — McKinsey/BCG 风格
- 🎓 **学术风** — 论文答辩、研究汇报
- 🌙 **禅意风** — 极简东方美学
- 🎨 **杂志风** — 图文并茂
- 💻 **科技风** — SaaS/产品发布
- 🌿 **自然风** — 纪录片风格

### 3️⃣ AI 编辑器集成

| 工具 | 评分 | 说明 |
|------|:----:|------|
| **[Claude Code](https://claude.ai/)** | ⭐⭐⭐ | 最佳效果 — 原生 Opus，最大上下文 |
| [Cursor](https://cursor.sh/) | ⭐⭐ | 不错的替代方案 |
| [VS Code + Copilot](https://code.visualstudio.com/) | ⭐⭐ | 主流选择 |
| **[OpenClaw](https://openclaw.ai/)** | ⭐⭐⭐ | **推荐** — 工作流自动化 |

### 4️⃣ OpenClaw 工作流集成

```
你：从这个季度报告生成一个 PPT

AI：好的，让我确认设计规格：
    [模板] 顶级咨询风
    [格式] PPT 16:9
    [页数] 8-10 页
    ...
    
    ✅ 已生成：Q3_Report_20260407.pptx
```

---

## 📖 使用场景

- 🎯 **商业汇报** — 季度总结、战略规划
- 🎓 **学术答辩** — 论文答辩、研究汇报
- 📊 **数据分析** — 可视化报告
- 🚀 **产品发布** — 新品介绍、路演
- 📚 **培训课件** — 企业培训、教学
- 📝 **内容营销** — 白皮书、案例研究

---

## 🎨 示例库

查看 [`examples/`](./examples/) — **15 个项目，229 页**已验证示例：

- 顶级咨询风 × 5（Anthropic AI、心理治疗、财政分析等）
- 学术风 × 2（论文格式、医学研究）
- 禅意风 × 1（金刚经研究）
- 科技风 × 3（Git 介绍、AI 编程工具对比）
- 自然风 × 1（野生动物纪录片）
- 杂志风 × 1（园艺指南）

---

## 🛠️ 安装指南

### 系统要求

- **Python** 3.8+（必需）
- **Node.js** 18+（可选 — 用于微信文章转换）
- **Pandoc**（可选 — 用于 DOCX/EPUB 转换）

### macOS

```bash
brew install python
brew install node      # 可选
brew install pandoc    # 可选
```

### Ubuntu/Debian

```bash
sudo apt install python3 python3-pip
sudo apt install nodejs npm    # 可选
sudo apt install pandoc        # 可选
```

### Windows

从官网下载安装：
- [Python](https://www.python.org/downloads/)
- [Node.js](https://nodejs.org/)（可选）
- [Pandoc](https://pandoc.org/)（可选）

---

## 🔧 高级用法

### 从现有项目导出

如果你已经有一个包含 `svg_final/` 目录的项目：

```bash
python3 skills/ppt-master/scripts/svg_to_pptx.py <项目路径> -s final
```

### 初始化新项目

```bash
python3 skills/ppt-master/scripts/project_manager.py init my_project --format ppt169
```

### OpenClaw Skill 集成

1. 将本仓库克隆到 OpenClaw 工作区
2. Skill 会被自动检测（`skills/PPTskill/SKILL.md`）
3. 直接对话：`"从这个文档生成一个 PPT"`

---

## 🗺️ Roadmap

- [x] 核心 PPT 生成能力
- [x] 10+ 专业模板
- [x] OpenClaw 集成
- [x] 中英双语文档
- [ ] 一键安装脚本
- [ ] GitHub Actions CI/CD
- [ ] 视频教程
- [ ] 更多模板（产品发布、融资路演）
- [ ] Web UI（可选）

---

## 🤝 贡献指南

欢迎贡献！请：

1. Fork 本仓库
2. 创建特性分支（`git checkout -b feature/AmazingFeature`）
3. 提交改动（`git commit -m 'Add some AmazingFeature'`）
4. 推送到分支（`git push origin feature/AmazingFeature`）
5. 提交 Pull Request

**贡献方向**：
- 新增模板风格
- 优化工作流集成
- 补充文档和示例
- Bug 修复

---

## 📝 已知限制

- 完整依赖安装可能因 `pycairo` / `cairo` 要求而失败
  - ⚠️ 这**不会**阻塞核心 PPT 导出功能
- DOCX/EPUB 转换需要 `pandoc`（可选）
- 需要 Office 2016+ 打开生成的 PPTX

---

## 🎯 设计哲学

遵循实用工程原则：

1. **首先验证最短工作路径**
2. **删除不必要的复杂性**
3. **稳定工作流**
4. **只在证明有价值后才自动化**

---

## 🙏 致谢

所有核心 PPT 生成能力来自优秀的上游项目：

- **[hugohe3/ppt-master](https://github.com/hugohe3/ppt-master)** — 感谢原作者的杰出工作

本分支专注于：
- 工作流集成优化
- OpenClaw 兼容性
- 实用文档和示例

---

## 👨‍💻 作者

**AI酋长Andy** | AI 产品专家，前腾讯/百度 AI PM，OpenClaw 深度用户

[![微信](https://img.shields.io/badge/微信-AIPMAndy-green)](https://github.com/AIPMAndy)
[![GitHub](https://img.shields.io/badge/GitHub-AIPMAndy-blue)](https://github.com/AIPMAndy)

---

## 📄 许可证

MIT License（与上游相同）

本仓库包含工作流文档和集成改进。
请尊重上游仓库的许可证和署名要求。

---

## 🔗 相关链接

- **上游项目**：https://github.com/hugohe3/ppt-master
- **本分支**：https://github.com/AIPMAndy/PPTskill
- **OpenClaw**：https://openclaw.ai/
- **在线示例**：https://hugohe3.github.io/ppt-master/

---

<div align="center">

**如果这个项目对你有帮助，请给个 ⭐ Star！**

让更多人发现这个工具 🚀

</div>
