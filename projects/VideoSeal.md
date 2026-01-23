---
layout: project
type: project
image: img/cotton/cotton-square.png
title: "Cotton"
date: 2025
published: true
labels:
  - Python
  - PyTorch
  - Neural Watermarking
summary: "Analyzing how robust Meta's VideoSeal watermarks are to noise and repeated watermarking. This was done as part of my contribution to my ECE 296 Sophomore Project."
---

<img class="img-fluid" src="../img/cotton/cotton-header.png">

For this lab project, our team worked with Meta’s VideoSeal, a neural watermarking system that hides binary messages in images and videos so that ownership and authenticity can be verified later. We set up the official VideoSeal codebase on a remote Linux server and built a pipeline that embeds a watermark, runs different “attacks” on the watermarked media, and then tries to recover the original bit string. The main goal was to see how well the watermark survives realistic changes while keeping the media visually similar, using bit accuracy, PSNR, and SSIM as our primary metrics.

Most of my work focused on understanding and running the image and video pipelines for two key attack types: adding Gaussian noise and applying repeated watermarking (second and third passes). I traced how VideoSeal takes in a clean image/video and a binary message, produces a watermarked version, and then decodes the message after various distortions. I also dealt with practical issues like environment setup, kernels, and paths in the repo, and helped interpret how the different attacks impacted watermark recovery and visual quality for use in our final poster.

<hr>

<pre>
Input media + binary message A
        │
        ▼
 VideoSeal embed
        │
        ├─► Watermarked image/video (baseline: detect A)
        │
        ├─► + Gaussian noise (vary σ) → detect → bit accuracy vs σ
        │
        └─► Re-embed (message B) → detect → compare messages A, B
</pre>

<hr>
