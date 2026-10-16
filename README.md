# DILLO — Describe-Then-Act

Official project website for **Describe-Then-Act: Proactive Agent Steering via Distilled Language-Action World Models**, accepted at ECCV 2026.

DILLO is a distilled language-action world model that predicts human-readable outcomes directly from a policy's latent state and proposed action chunks. These predictions allow an embodied agent to identify and reject risky actions before executing them, without generating future visual observations.

## Links

- [Project website](https://lucaromani98.github.io/dillo-website/)
- [Paper on arXiv](https://arxiv.org/abs/2603.23149)
- [Official DILLO repository](https://github.com/MaxPappa/DILLO)
- [DILLO-LIBERO dataset](https://huggingface.co/datasets/Sapienza/DILLO-LIBERO-dataset)
- [Released checkpoints](https://drive.google.com/drive/folders/10sKCwHCWn7quLJQCYrFr8885iK7muXGf?usp=sharing)

## Website contents

The project page presents:

- an overview of the describe-then-act framework;
- the training and inference pipeline;
- headline quantitative results;
- qualitative DILLO predictions on LIBERO trajectories;
- a reproduced comparison between an ACT policy and DILLO-guided action selection;
- links to the paper, code, dataset, and model checkpoints.

The qualitative gallery uses the released DILLO Gemma-3 1B model. Each example shows the proposed action outcome, DILLO's positive or negative verdict, and the corresponding trajectory. The steering comparison also includes an action candidate rejected before execution.

## Run locally

The website is static and requires no build step. From the repository root, run:

```bash
python3 -m http.server 8000
```

Then open [http://localhost:8000](http://localhost:8000).

## Repository structure

```text
.
├── index.html
└── static
    ├── css
    ├── images
    ├── js
    └── videos/qualitative
```

Metadata for the qualitative examples and reproduced rollouts is available in [`static/videos/qualitative/manifest.json`](static/videos/qualitative/manifest.json).

## Citation

```bibtex
@misc{pappa2026describethenact,
  title         = {Describe-Then-Act: Proactive Agent Steering via
                   Distilled Language-Action World Models},
  author        = {Massimiliano Pappa and Luca Romani and Valentino Sacco and
                   Alessio Palma and St\'ephane Lathuili\`ere and Fabio Galasso and
                   Xavier Alameda-Pineda and Indro Spinelli},
  year          = {2026},
  eprint        = {2603.23149},
  archivePrefix = {arXiv},
  primaryClass  = {cs.AI}
}
```
