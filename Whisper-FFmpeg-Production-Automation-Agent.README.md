# Whisper + FFmpeg Production Automation Agent

> Tool-use agent that ships polished video edits end-to-end: ingest → transcribe → caption → color → render.

[![Author](https://img.shields.io/badge/built%20by-Yaswanthkumar--8-ff2bd6?style=flat-square)](https://github.com/Yaswanthkumar-8)
[![Status](https://img.shields.io/badge/status-active-00f0ff?style=flat-square)](#)
![License](https://img.shields.io/badge/license-MIT-fff200?style=flat-square)

## ✨ Features

- Each production step modeled as a callable tool the planner can chain
- Whisper-driven cut suggestions for filler-word and silence removal (HITL review)
- Per-step checkpoints halt the pipeline on bad output instead of burning a render
- Containerised runner: same pipeline runs locally or on a GPU box for heavy passes

## 🧱 Tech Stack

`Python 3.11+` · `Whisper` · `FFmpeg` · `Click` · `Docker`

## 🚀 Quick start

```bash
git clone https://github.com/Yaswanthkumar-8/Whisper-FFmpeg-Production-Automation-Agent.git
cd Whisper-FFmpeg-Production-Automation-Agent
cp .env.example .env   # fill in the values below
# install + run
docker compose run --rm agent process ./projects/example
```

### Required environment variables

| Variable | Purpose |
| --- | --- |
| `OPENAI_API_KEY` | required |
| `WHISPER_MODEL` | default large-v3 |

## 📸 Screenshots

> Drop screenshots into `docs/screenshots/` and link them here.

| Overview | Architecture | Result |
| --- | --- | --- |
| ![overview](docs/screenshots/overview.png) | ![architecture](docs/screenshots/architecture.png) | ![result](docs/screenshots/result.png) |

## 🧭 Architecture

```text
[ Input ] → [ Orchestrator ] → [ Specialist tools ] → [ Output / artifact ]
```

See the case study on the portfolio for the full system diagram and decisions.

## 🗺 Roadmap

- [ ] Public demo deployment (Vercel / GitHub Pages)
- [ ] CI: lint, typecheck, smoke tests on PR
- [ ] Example dataset / project fixtures
- [ ] Walkthrough video in `docs/`

## 📄 License

MIT — see [`LICENSE`](LICENSE).

## 🙋 Author

**Yaswanth Kumar Saragadam** — AI/ML engineer & agentic systems builder
- GitHub: [@Yaswanthkumar-8](https://github.com/Yaswanthkumar-8)
- LinkedIn: [yaswanth-kumar-yk](https://linkedin.com/in/yaswanth-kumar-yk)
- Portfolio: https://yaswanthkumarsaragadam.lovable.app
