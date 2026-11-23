---
layout: archive
title: CV
permalink: /cv/
author_profile: true
redirect_from:
- /resume
---

{% include base_path %}

[Download the full CV as a PDF]({{ base_path }}/files/CV_Ronak_Kosti.pdf)

Experience
======

**Senior Research Engineer / Applied ML Scientist**, 404-GEN, Berlin, Germany  
*Jan 2025 – present*

Applied research on multimodal Text/Image-to-3D foundation models, world models, agent-orchestrated evals, and high-throughput reliable ML pipelines.

- Maintained and optimized an open-source text/image-to-mesh generator consistently in the top-5 on 3D Arena (Hugging Face).
- Delivered 33–50% faster inference than the baseline model and reduced VRAM from 96GB to 48GB with zero quality degradation; deterministic generation up to a quality bar.
- Applied reinforcement learning post-training after inference optimization to improve 3D mesh output quality, achieving **80% human-aligned quality** improvement over the baseline model, measured by preference votes.
- Deployed the text/image-to-mesh generator as a **production API service** called by an agent; a redundant cold-start trigger launches the model on another GPU on failure.

**Senior ML Scientist / Research Lead**, Picsart AI Research, Berlin, Germany  
*Nov 2022 – May 2024*

Project Lead for generative diffusion models (text-to-image, stylized typography, drag editing); shipped models to production serving millions of global users.

- Project Lead for stylized font generation using Stable Diffusion, LoRA adaptations, and model merging conditioned on SSL-DINO features; deployed to production serving millions of users.
- Solved high-precision 94-glyph font collage synthesis by optimizing cross-attention guidance for consistent style, scale, and character boundaries.
- Hands-on training, fine-tuning, and post-training of the stylized font generation model, plus optimizations for carrying the target styles into the final fonts.
- Pioneered interactive drag-based editing by optimizing DDIM inversion, motion priors, and diffusion U-Net feature maps for point-guided manipulation.

**ML Lead**, FAU Erlangen-Nürnberg & Philipps-Universität Marburg, Erlangen / Marburg, Germany  
*May 2019 – Oct 2022*

ML lead across postdoctoral appointments: multimodal modeling, generative pipelines, foundation-model auditing, and contrastive / domain-adaptation research.

- Multimodal modeling lead on the fotoMarburg corpus (1.7M images, DFG/SPP); applied generative AI and representation learning under severe data heterogeneity.
- Systematically probed CLIP, DINO, and VQGAN latent spaces; identified and published compositional, positional, and semantic biases in generative representations.
- Formulated semi-supervised, segmentation-guided GAN and diffusion synthesis pipelines for high-fidelity generation under data heterogeneity.
- Built automated cleaning, deduplication, and feature extraction pipelines across 1.7M heterogeneous assets for downstream multimodal training.

**Doctoral Researcher**, Universitat Oberta de Catalunya (UOC), Barcelona, Spain  
*Oct 2015 – Sep 2019*

Thesis: Visual Scene Context in Emotion Perception. Multimodal affective understanding, dataset curation, and fusion modeling.

- Created and open-sourced EMOTIC (34K subjects, 26 categorical + 3 continuous VAD labels); built AMT crowdsourcing and QC pipelines (IEEE TPAMI & CVPR, 1,000+ citations).
- Architected multi-branch deep networks fusing facial, bodily, and environmental scene context for affective understanding.
- Released reproducible training, evaluation, and preprocessing codebases adopted widely across the affective computing community.

Education
======

- **Ph.D. in Computer Vision & Machine Learning**, Universitat Oberta de Catalunya (UOC), Barcelona, Spain, Oct 2015 – Sep 2019. Excellent CUM LAUDE.  
  Thesis: *Visual Scene Context in Emotion Perception (Advisor: Prof. Agata Lapedriza)*
- **M.Sc. in Machine Intelligence**, DA-IICT, Gandhinagar, India, Jul 2012 – Jul 2014. Grade: Excellent.  
  Thesis: *Depth from a Single Image via Neural Networks*
- **B.Eng. in Electronics Engineering**, SVNIT, Surat, India, Jun 2007 – May 2011. GPA: 7.52 / 10.0.

Skills
======

- **Generative & Multimodal:** Foundation Models, Diffusion (DDIM, U-Net, DiT), Multimodal Fusion (Vision, Text, Audio), Cross-Modal Alignment, Text/Image-to-3D, World Models, GANs
- **Training & Adaptation:** Python, PyTorch, Supervised Fine-Tuning (SFT), Post-Training (RLHF), LoRA / PEFT, Model Merging, Knowledge Distillation, Supervised Contrastive Learning, Self-Supervised Learning (DINO)
- **ML Pipelines, Agents & Infra:** Agent Orchestration Workflows, End-to-End ML Pipelines, Distributed Multi-GPU Training, GCP, AWS, Runpod, Verda, vLLM Serving, Vector Databases, Docker, Linux/Bash, Git, CI/CD Regression QA
- **Evals & Benchmarking:** Automated Benchmark Harnesses, LLM-as-a-Judge, Human-in-the-Loop Pipelines (AMT), A/B Testing Orchestration, Perceptual Metrics (VQAScore, CLIPScore)

Publications
======

<ul>{% for post in site.publications reversed %}
  {% include archive-single-cv.html %}
{% endfor %}</ul>

Honors and service
======

- **Grant (PI)** — Emerging Talent Initiative (ETI), FAU (€15k) — Multimodal (Audio, Text, Visual) Emotion Recognition (Jul 2020–Sep 2021).
- **Award** — 3rd Prize, Best Scientific Work — Few-shot Unsupervised Multimodal Segmentation (BVM 2022).
- Organization — Co-Chair & Organizer: SUMAC Workshop at ACM Multimedia (2020–2024); Co-Organizer & AMT Annotation Lead: ODOR Challenge at ICPR 2022.
- Mentorship — Supervised 10+ Ph.D., Master's, and Bachelor's theses in generative modeling and computer vision.
- **Reviewer** — CVPR, ICCV, NeurIPS, ICLR, WACV, ACM Multimedia, ICPR, IEEE TIP, IEEE TMM.
