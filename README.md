# PPTskill — AI-Powered PPTX Generation (Optimized Fork)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Based on ppt-master](https://img.shields.io/badge/based%20on-ppt--master-blue)](https://github.com/hugohe3/ppt-master)

English | [中文](./README_CN.md)

**PPTskill** is an optimized fork of [`hugohe3/ppt-master`](https://github.com/hugohe3/ppt-master), focused on practical workflow integration and OpenClaw compatibility.

Drop in a PDF, DOCX, URL, or Markdown — get back a **natively editable PowerPoint** with real shapes, real text boxes, and real charts. Not images. Click anything and edit it.

## What's Different from Upstream

This fork adds:

- ✅ **OpenClaw skill integration** — works seamlessly in OpenClaw workflows
- ✅ **Simplified setup** — clearer dependency management
- ✅ **Workflow documentation** — practical usage patterns for real projects
- ✅ **Tested examples** — verified working paths on macOS/Linux

All core PPT generation capability comes from the excellent upstream project. This fork focuses on making it easier to use in production workflows.

## Quick Start

### 1. Install

**Required:** [Python](https://www.python.org/downloads/) 3.8+  
**Optional:** [Node.js](https://nodejs.org/) 18+ (for WeChat page conversion) · [Pandoc](https://pandoc.org/) (for DOCX/EPUB conversion)

```bash
# macOS
brew install python
brew install node                # optional
brew install pandoc              # optional

# Ubuntu/Debian
sudo apt install python3 python3-pip
sudo apt install nodejs npm      # optional
sudo apt install pandoc          # optional
```

```bash
git clone https://github.com/AIPMAndy/PPTskill.git
cd PPTskill
pip install -r requirements.txt
```

### 2. Pick an AI Editor

| Tool | Rating | Notes |
|------|:------:|-------|
| **[Claude Code](https://claude.ai/)** | ⭐⭐⭐ | Best results — native Opus, largest context |
| [Cursor](https://cursor.sh/) / [VS Code + Copilot](https://code.visualstudio.com/) | ⭐⭐ | Good alternatives |
| **[OpenClaw](https://openclaw.ai/)** | ⭐⭐⭐ | Recommended for workflow automation |

### 3. Create

Open the AI chat panel and describe what you want:

```
You: I have a Q3 quarterly report that needs to be made into a PPT

AI:  Sure. Let's confirm the design spec:
     [Template] B) No template
     [Format]   PPT 16:9
     [Pages]    8-10 pages
     ...
```

The AI handles everything — content analysis, visual design, SVG generation, and PPTX export.

> **Output:** The `.pptx` file contains native shapes — directly editable. A second `_svg.pptx` reference file is also generated (use "Convert to Shape" in PowerPoint to edit). Requires Office 2016+.

### 4. Export from Existing Project

If you already have a project with `svg_final/` directory:

```bash
python3 skills/ppt-master/scripts/svg_to_pptx.py <project_path> -s final
```

Example:

```bash
python3 skills/ppt-master/scripts/svg_to_pptx.py examples/ppt169_顶级咨询风_构建有效AI代理_Anthropic -s final
```

## Gallery

See [`examples/`](./examples/) — 15 projects, 229 pages of verified working examples.

## OpenClaw Integration

If you're using OpenClaw, this repo includes a skill definition at `skills/PPTskill/SKILL.md`.

To use it:

1. Clone this repo to your OpenClaw workspace
2. The skill will be auto-detected
3. Ask your agent: "Generate a PPT from this document"

## Known Limitations

- Full dependency install may fail on some systems due to `pycairo` / `cairo` requirements
- This does **not** block core PPT export functionality
- DOCX/EPUB conversion requires `pandoc` (optional)

## Verified Working Path

Tested on:

- macOS (Apple Silicon + Intel)
- Python 3.11
- Upstream commit: `e0d2208`

Core export path confirmed working:

- ✅ `svg_final/` → editable `.pptx`
- ✅ Native PPTX generation
- ✅ Example projects export successfully

## Philosophy

Following practical engineering principles:

1. **Verify the shortest working path first**
2. **Remove unnecessary complexity**
3. **Stabilize the workflow**
4. **Automate only after it's proven valuable**

## Upstream Credit

All major PPT generation capability comes from:

- **[hugohe3/ppt-master](https://github.com/hugohe3/ppt-master)**

This fork exists to make that excellent work easier to integrate into real workflows.

## Contributing

Contributions welcome! Please:

- Keep changes focused on workflow improvements
- Document what you've tested
- Respect the upstream project's design decisions

## License

MIT License (same as upstream)

This repository contains workflow documentation and integration improvements.
Please respect the upstream repository's license and attribution requirements.

## Links

- **Upstream:** https://github.com/hugohe3/ppt-master
- **This Fork:** https://github.com/AIPMAndy/PPTskill
- **OpenClaw:** https://openclaw.ai/
