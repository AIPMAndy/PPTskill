<div align="center">

# 🎨 PPTskill

**AI-Powered Native Editable PPTX Generation — Professional Presentations Without Design Skills**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Based on ppt-master](https://img.shields.io/badge/based%20on-ppt--master-blue)](https://github.com/hugohe3/ppt-master)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![OpenClaw Compatible](https://img.shields.io/badge/OpenClaw-compatible-green)](https://openclaw.ai/)

**English** | [简体中文](./README.md)

<img src="docs/assets/screenshots/preview_magazine_garden.png" width="600" alt="PPTskill Demo">

</div>

---

## 🆚 Why PPTskill?

| Feature | Traditional PPT | Online AI PPT | **PPTskill** |
|---------|:---------------:|:-------------:|:------------:|
| Native Editable | ✅ | ❌ Image/SVG | ✅ **Real Shapes** |
| AI-Powered | ❌ | ✅ | ✅ |
| Local/Private | ✅ | ❌ | ✅ **Privacy First** |
| Workflow Integration | ❌ | ❌ | ✅ **OpenClaw/Cursor** |
| Open Source | ❌ | ❌ | ✅ **MIT License** |
| Multiple Styles | ⚠️ Manual | ⚠️ Limited | ✅ **10+ Templates** |

**Key Difference**: Outputs **real PowerPoint objects** (DrawingML), not images or embedded SVGs. Click any element to edit directly.

---

## 🚀 Quick Start (30 seconds)

```bash
# 1. Clone repository
git clone https://github.com/AIPMAndy/PPTskill.git
cd PPTskill

# 2. Install dependencies
pip install -r requirements.txt

# 3. Export example PPT
python3 skills/ppt-master/scripts/svg_to_pptx.py examples/ppt169_顶级咨询风_构建有效AI代理_Anthropic -s final

# ✅ Done! Find generated .pptx in examples/ directory
```

**Output**:
- `project_timestamp.pptx` — Native editable version (recommended)
- `project_timestamp_svg.pptx` — SVG reference version

---

## 💡 Core Features

### 1️⃣ Multiple Input Formats

- 📄 **PDF** — Research papers, reports
- 📝 **DOCX** — Word documents
- 🌐 **URL** — Web pages, blog posts
- 📋 **Markdown** — Technical documentation

### 2️⃣ 10+ Professional Templates

- 🏢 **Consulting Style** — McKinsey/BCG inspired
- 🎓 **Academic Style** — Thesis defense, research
- 🌙 **Zen Style** — Minimalist Eastern aesthetics
- 🎨 **Magazine Style** — Photo-rich layouts
- 💻 **Tech Style** — SaaS/product launches
- 🌿 **Nature Style** — Documentary aesthetics

### 3️⃣ AI Editor Integration

| Tool | Rating | Notes |
|------|:------:|-------|
| **[Claude Code](https://claude.ai/)** | ⭐⭐⭐ | Best results — native Opus, largest context |
| [Cursor](https://cursor.sh/) | ⭐⭐ | Great alternative |
| [VS Code + Copilot](https://code.visualstudio.com/) | ⭐⭐ | Mainstream choice |
| **[OpenClaw](https://openclaw.ai/)** | ⭐⭐⭐ | **Recommended** — workflow automation |

### 4️⃣ OpenClaw Workflow Integration

```
You: Generate a PPT from this quarterly report

AI:  Sure. Let me confirm the design spec:
     [Template] Consulting Style
     [Format]   PPT 16:9
     [Pages]    8-10 pages
     ...
     
     ✅ Generated: Q3_Report_20260407.pptx
```

---

## 📖 Use Cases

- 🎯 **Business Reports** — Quarterly reviews, strategic planning
- 🎓 **Academic Defense** — Thesis presentations, research talks
- 📊 **Data Analysis** — Visualization reports
- 🚀 **Product Launches** — New product intros, pitch decks
- 📚 **Training Materials** — Corporate training, teaching
- 📝 **Content Marketing** — White papers, case studies

---

## 🎨 Example Gallery

See [`examples/`](./examples/) — **15 projects, 229 pages** of verified examples:

- Consulting Style × 5 (Anthropic AI, Psychology, Finance, etc.)
- Academic Style × 2 (Thesis format, Medical research)
- Zen Style × 1 (Buddhist scripture study)
- Tech Style × 3 (Git intro, AI coding tools comparison)
- Nature Style × 1 (Wildlife documentary)
- Magazine Style × 1 (Gardening guide)

---

## 🛠️ Installation Guide

### System Requirements

- **Python** 3.8+ (required)
- **Node.js** 18+ (optional — for WeChat article conversion)
- **Pandoc** (optional — for DOCX/EPUB conversion)

### macOS

```bash
brew install python
brew install node      # optional
brew install pandoc    # optional
```

### Ubuntu/Debian

```bash
sudo apt install python3 python3-pip
sudo apt install nodejs npm    # optional
sudo apt install pandoc        # optional
```

### Windows

Download from official sites:
- [Python](https://www.python.org/downloads/)
- [Node.js](https://nodejs.org/) (optional)
- [Pandoc](https://pandoc.org/) (optional)

---

## 🔧 Advanced Usage

### Export from Existing Project

If you have a project with `svg_final/` directory:

```bash
python3 skills/ppt-master/scripts/svg_to_pptx.py <project_path> -s final
```

### Initialize New Project

```bash
python3 skills/ppt-master/scripts/project_manager.py init my_project --format ppt169
```

### OpenClaw Skill Integration

1. Clone this repo to your OpenClaw workspace
2. Skill auto-detected (`skills/PPTskill/SKILL.md`)
3. Chat directly: `"Generate a PPT from this document"`

---

## 🗺️ Roadmap

- [x] Core PPT generation capability
- [x] 10+ professional templates
- [x] OpenClaw integration
- [x] Bilingual documentation (EN/CN)
- [ ] One-click installation script
- [ ] GitHub Actions CI/CD
- [ ] Video tutorials
- [ ] More templates (pitch decks, fundraising)
- [ ] Web UI (optional)

---

## 🤝 Contributing

Contributions welcome! Please:

1. Fork this repository
2. Create feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Submit Pull Request

**Contribution areas**:
- New template styles
- Workflow integration improvements
- Documentation and examples
- Bug fixes

---

## 📝 Known Limitations

- Full dependency install may fail due to `pycairo` / `cairo` requirements
  - ⚠️ This does **not** block core PPT export functionality
- DOCX/EPUB conversion requires `pandoc` (optional)
- Requires Office 2016+ to open generated PPTX

---

## 🎯 Design Philosophy

Following practical engineering principles:

1. **Verify shortest working path first**
2. **Remove unnecessary complexity**
3. **Stabilize the workflow**
4. **Automate only after proven valuable**

---

## 🙏 Acknowledgments

All core PPT generation capability comes from the excellent upstream project:

- **[hugohe3/ppt-master](https://github.com/hugohe3/ppt-master)** — Thanks to the original author for outstanding work

This fork focuses on:
- Workflow integration optimization
- OpenClaw compatibility
- Practical documentation and examples

---

## 👨‍💻 Author

**AI Chief Andy** | AI Product Expert, Former Tencent/Baidu AI PM, OpenClaw Power User

[![WeChat](https://img.shields.io/badge/WeChat-AIPMAndy-green)](https://github.com/AIPMAndy)
[![GitHub](https://img.shields.io/badge/GitHub-AIPMAndy-blue)](https://github.com/AIPMAndy)

---

## 📄 License

MIT License (same as upstream)

This repository contains workflow documentation and integration improvements.
Please respect the upstream repository's license and attribution requirements.

---

## 🔗 Related Links

- **Upstream Project**: https://github.com/hugohe3/ppt-master
- **This Fork**: https://github.com/AIPMAndy/PPTskill
- **OpenClaw**: https://openclaw.ai/
- **Live Examples**: https://hugohe3.github.io/ppt-master/

---

<div align="center">

**If this project helps you, please give it a ⭐ Star!**

Help more people discover this tool 🚀

</div>
