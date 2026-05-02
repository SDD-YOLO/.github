🏭 SDD-YOLO

Self-Developed Detection YOLO —— 面向工业表面缺陷检测与边缘部署的研究框架

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)
[![Python](https://img.shields.io/badge/Python-3.10%2B-blue)](https://www.python.org/)
[![PyTorch](https://img.shields.io/badge/PyTorch-2.0%2B-orange)](https://pytorch.org/)
[![React](https://img.shields.io/badge/React-18-61DAFB?logo=react)](https://react.dev/)

---

概览

SDD-YOLO 是一个面向地对空反无人机检测的研究型框架，专注于小目标识别、知识蒸馏与边缘设备部署。我们致力于弥合高精度深度学习模型与现实场景之间的差距——在这些场景中，计算资源受限，且高精确度的检出至关重要。

我们的工作覆盖完整的技术链路：从精心整理的数据集、高效的模型架构，到一键式训练工具、基于 Web 的可视化界面，以及边缘性能分析。

> 🚧 我们正处于早期开发阶段。欢迎关注我们的进展，并为感兴趣的仓库点亮 Star。

---

代码仓库

仓库	说明	状态	
[`EdgeDistillDet`](https://github.com/SDD-YOLO/EdgeDistillDet)	支持 Web UI 与 AI Agent 的蒸馏训练及评估工具包 —— 兼容 RK3588、Ascend310、CPU/GPU 边缘设备性能分析	✅ v1.0.5 已发布	
`sdd-yolo-datasets`	精心整理的数据集，提供统一标注格式	🚧 进行中	
`sdd-yolo`	核心模型架构 —— 轻量级骨干网络设计与小目标检测头优化	🚧 进行中	

---

EdgeDistillDet —— 我们的首个里程碑

EdgeDistillDet 是 SDD-YOLO 生态系统中首个公开发布的组件。它提供了：

- 🧠 教师-学生知识蒸馏 —— 基于 YAML 配置的训练流程，支持断点续训
- 📊 Web 可视化工作台 —— 基于 React + FastAPI 的训练进度与指标可视化
- 🔍 边缘设备性能分析 —— 在 RK3588、Ascend310、CPU 及 GPU 上进行模型基准测试，助力部署决策
- 🤖 AI Agent 集成 —— Agent 辅助的训练工作流与基于 RAG 的文档检索
- ⚡ CLI 工具 —— 一条命令完成训练、评估、分析与性能分析

```bash
pip install -r requirements.txt
edgedistilldet train --config configs/distill_config.yaml
```

👉 [开始使用 EdgeDistillDet](https://github.com/SDD-YOLO/EdgeDistillDet)

---

路线图

```
第一阶段 —— 工具与基础设施   🔄 进行中
├── EdgeDistillDet Web UI 与 CLI    ✅ 已发布
└── CI/CD 与发布自动化              ✅ 活跃维护

第二阶段 —— 数据与模型       📅 已规划
├── 工业缺陷数据集           🚧 进行中
├── 轻量化 YOLO 骨干网络     🚧 进行中
└── 小目标检测头             🚧 进行中

第三阶段 —— 整合             📅 未来
├── 端到端缺陷检测流水线
└── 边缘部署包（RK、Ascend）
```

---

快速开始

> EdgeDistillDet 已可投入使用。其他组件敬请期待后续发布。

```bash
# 克隆 EdgeDistillDet
git clone https://github.com/SDD-YOLO/EdgeDistillDet
cd EdgeDistillDet

# 安装（建议 Python 3.10+）
pip install -r requirements.txt

# 启动 Web UI
cd web && npm ci && npm run build && cd ..
python web/app.py
# 访问 http://127.0.0.1:5000
```

---

引用

如果您在研究中使用了 EdgeDistillDet 或 SDD-YOLO 的任何后续组件，请引用：

```bibtex
@software{sdd_yolo_2026,
  author = {SDD-YOLO Team},
  title = {SDD-YOLO: Self-Developed Detection YOLO for Industrial Surface Defect Detection},
  url = {https://github.com/SDD-YOLO},
  year = {2026}
}
```

---

许可证

SDD-YOLO 组织下的所有仓库均基于 [Apache 2.0 许可证](LICENSE) 发布。

---

⭐ 为我们点亮 Star，及时获取最新进展！
