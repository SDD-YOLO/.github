🏭 SDD-YOLO

Self-Developed Detection YOLO — Research Framework for Industrial Surface Defect Detection & Edge Deployment

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)
[![Python](https://img.shields.io/badge/Python-3.10%2B-blue)](https://www.python.org/)
[![PyTorch](https://img.shields.io/badge/PyTorch-2.0%2B-orange)](https://pytorch.org/)
[![React](https://img.shields.io/badge/React-18-61DAFB?logo=react)](https://react.dev/)

---

Overview

SDD-YOLO is a research-driven framework dedicated to industrial surface defect detection, with a focus on small-target recognition, knowledge distillation, and edge-device deployment. We aim to bridge the gap between high-accuracy deep learning models and real-world manufacturing constraints where compute resources are limited and millimeter-level defects matter.

Our work spans the full pipeline — from curated industrial datasets and efficient model architectures, to one-click training tools with web-based visualization and edge performance profiling.

> 🚧 We are in active early-stage development. Follow our progress and star the repos you find interesting.

---

Repositories

Repository	Description	Status	
[`EdgeDistillDet`](https://github.com/SDD-YOLO/EdgeDistillDet)	Distillation training & evaluation toolkit with Web UI and AI Agent — supports RK3588, Ascend310, CPU/GPU edge profiling	✅ v1.0.5 Available	
`sdd-yolo-datasets`	Curated industrial surface defect datasets with unified annotations	🚧 WIP	
`sdd-yolo`	Core model architecture — lightweight backbone design and small-target head optimization	🚧 WIP	

EdgeDistillDet — Our First Milestone

EdgeDistillDet is the first publicly available component of the SDD-YOLO ecosystem. It provides:

- 🧠 Teacher-Student Distillation — YAML-driven training with resume support
- 📊 Web-based Workbench — React + FastAPI visualization for training progress and metrics
- 🔍 Edge Device Profiling — Benchmark models on RK3588, Ascend310, CPU, and GPU before deployment
- 🤖 AI Agent Integration — Agent-assisted training workflow and documentation retrieval (RAG)
- ⚡ CLI Tools — One-command train, eval, analyze, and profile

```bash
pip install -r requirements.txt
edgedistilldet train --config configs/distill_config.yaml
```

👉 [Get Started with EdgeDistillDet](https://github.com/SDD-YOLO/EdgeDistillDet)

---

Roadmap

```
Phase 1 — Tools & Infrastructure   🔄 In Progress
├── EdgeDistillDet Web UI & CLI    ✅ Released
└── CI/CD & Release Automation     ✅ Active

Phase 2 — Data & Models            📅 Planned
├── Industrial defect datasets     🚧 WIP
├── Lightweight YOLO backbone      🚧 WIP
└── Small-target detection head    🚧 WIP

Phase 3 — Integration              📅 Future
├── End-to-end defect pipeline
└── Edge deployment packages (RK, Ascend)
```

---

Quick Start

> EdgeDistillDet is ready to use. For other components, please stay tuned for upcoming releases.

```bash
# Clone EdgeDistillDet
git clone https://github.com/SDD-YOLO/EdgeDistillDet.git
cd EdgeDistillDet

# Install (Python 3.10+ recommended)
pip install -r requirements.txt

# Launch Web UI
cd web && npm ci && npm run build && cd ..
python web/app.py
# Visit http://127.0.0.1:5000
```

---

Citation

If you use EdgeDistillDet or any future component of SDD-YOLO in your research, please cite:

```bibtex
@software{sdd_yolo_2026,
  author = {SDD-YOLO Team},
  title = {SDD-YOLO: Self-Developed Detection YOLO for Industrial Surface Defect Detection},
  url = {https://github.com/SDD-YOLO},
  year = {2026}
}
```

---

License

All repositories under the SDD-YOLO organization are released under the [Apache 2.0 License](LICENSE).

---

⭐ Star us to stay updated on our progress!
