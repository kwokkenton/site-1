---
layout: single
title: "My Research interests"
date: 2025-06-04 12:00:00 +0000
excerpt: an evolving literature review based on my current research interests
read_time: true
categories: thoughts
mathjax: true
---

> This is my attempt to understand some gaps in research that I currently find interesting in. At the moment they revolve around computer vision and machine learning in biology. Last updated: June 2025.

## Computer Vision: World models and 3D

There has traditionally been a gap between the geometric reconstruction based side of computer vision with recognition/ reorganisation side which has shifted to neural network based. Transformer based architectures are now used to tackle the [geometry based problem (VGGT, 2025)](https://arxiv.org/pdf/2503.11651), which is orders of magnitude quicker than other techniques such as structure from motion. Now this is present, it would be interested to tap into its embeddings to see what 'understanding' of the visual world it has.

Other topics: Neural Radiance Fields, 3/4D Gaussian Splatting

Groups: [Visual Geometry Group, Oxford](https://www.robots.ox.ac.uk/~vgg/research/)

## Computer Vision: For science

A large part of the computer vision community is focused on visual perception and reasoning.

[Cell painting (2016)](https://www.nature.com/articles/s41596-023-00840-9) is an imaging-based cellular assay based on morphology (size, shape) that can be used to quantify the effects of chemical or genetic 'perturbations' to the cells.

Image processing/ analysis techniques are maturing now (at least in 2D), and research is focused on obtaining an **understanding** of the objects in images themselves.

## Computational Photography and Imaging

the joint design of optics and algorithms to get the result you want. Applications in cell microscopy and neuroscience. See Laura Waller, Na Ji.

## Machine Learning for biology and medicine

Human scientists can pose questions/ hypotheses, do experiments, get data and learn from the data. Machines and computers are getting to the point where it can do the same. Centres such as the CZ Biohub, and big pharma are are constructing high throughput profiling platforms for basic research as well as applied screening.

Biological data is tricky as unlike internet images, many times the datasets are small, require expert annotation, and experiments are costly to run.

The world is inherently multimodal. Part of this is learning a 'joint representation' and hence developing understanding of the phenomenon itself.

Generative design of molecules. Graph neural networks lend naturally to molecules. How can it be applied in synthetic biology and therapeutics?

Meetings

- [Computer vision for drug discovery at CVPR](https://cvdd-cvpr25.github.io/)
- [Learning Meaningful Representations of Life (LMRL) at ICLR 2025](https://www.lmrl.org/)
