# DexGrasp-Anything-Unofficial

> Unofficial PyTorch implementation starter for **DexGrasp Anything: Towards Universal Robotic Dexterous Grasping with Physics Awareness** (CVPR 2025).
>
> If this repo saves you reading / reproduction time, please star it and follow [@StaryMoon](https://github.com/StaryMoon). I am building honest open reproduction starters for recent CVPR papers.

## Status

This repository is an **independent, unofficial, work-in-progress starter**.

- Paper: [DexGrasp Anything: Towards Universal Robotic Dexterous Grasping with Physics Awareness](https://openaccess.thecvf.com/content/CVPR2025/html/Zhong_DexGrasp_Anything_Towards_Universal_Robotic_Dexterous_Grasping_with_Physics_Awareness_CVPR_2025_paper.html)
- Venue: CVPR 2025
- Reproduction status: **benchmarks are not reproduced yet**
- Relationship to authors: this repo is not official and is not affiliated with the paper authors.

## What Is Implemented

This v0.1.0 starter implements a compact, readable scaffold inspired by the paper:

- observation encoder
- language/goal conditioning
- action policy head
- toy behavior-cloning loss
- smoke-test script

The goal is to make the high-level idea easy to inspect, fork, and improve.

## What Is Not Implemented Yet

- robot simulator integration
- real manipulation dataset
- physics-aware constraints
- official success-rate reproduction

## Quick Start

```bash
git clone https://github.com/StaryMoon/DexGrasp-Anything-Unofficial.git
cd DexGrasp-Anything-Unofficial
pip install -r requirements.txt
python scripts/smoke_test.py
```

Expected output includes:

```text
loss: ...
actions: torch.Size([2, 8, 7])
```

## Minimal Usage

```python
import torch
from dexgrasp_anything_unofficial import UnofficialStarter

image = torch.rand(2, 3, 64, 64)
model = UnofficialStarter(kind="robot")
out = model(image)
```

## Roadmap

- [ ] Replace toy modules with a closer implementation of the paper.
- [ ] Add dataset loader and config files.
- [ ] Add metric scripts and visualization.
- [ ] Reproduce a small benchmark or ablation table.
- [ ] Add pretrained weights once experiments are stable.

## Search Tags

cvpr-2025, robotics, dexterous-grasping, physics-aware, pytorch, unofficial-implementation

## Citation

Please cite the original paper if you use the method. This repo is only an unofficial starter and does not replace the paper.

## License

MIT License. The original paper and official materials remain owned by their respective authors / publishers.
