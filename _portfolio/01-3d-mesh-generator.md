---
title: Text/image-to-mesh generator
collection: portfolio
permalink: /portfolio/3d-mesh-generator/
excerpt: 'Open-source 3D generator, consistently top-5 on Hugging Face 3D Arena. Made it 33–50% faster at half the VRAM, then post-trained it with RL.


  *404-GEN · 2025–present*'
tags:
- 3D generation
- inference optimization
- RLHF
- serving
---

*404-GEN · 2025–present*

Open-source 3D generator, consistently top-5 on Hugging Face 3D Arena. Made it 33–50% faster at half the VRAM, then post-trained it with RL.

## What I did

- Maintained and optimized an open-source text/image-to-mesh generator consistently in the top-5 on 3D Arena (Hugging Face).
- Delivered 33–50% faster inference than the baseline model and reduced VRAM from 96GB to 48GB with zero quality degradation; deterministic generation up to a quality bar.
- Applied reinforcement learning post-training after inference optimization to improve 3D mesh output quality, achieving **80% human-aligned quality** improvement over the baseline model, measured by preference votes.
- Deployed the text/image-to-mesh generator as a **production API service** called by an agent; a redundant cold-start trigger launches the model on another GPU on failure.
- Served models in production with **vLLM**, using its compilation step so inference runs faster after compilation.

## Links

- [Code](https://github.com/404-Repo/404-base-miner-mesh)
- [3D Arena leaderboard](https://huggingface.co/spaces/3d-arena/3d-arena)
