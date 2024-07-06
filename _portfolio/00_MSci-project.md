---
title: "MSci work- volumetric bioimaging using OPT"
excerpt: "Doing benchtop optics, programming and analysis for biology!"
header:
  image: files/opt/embryo.jpg
  teaser: files/opt/embryo.jpg
sidebar:
  - title: "Role"
    image: https://pxl-imperialacuk.terminalfour.net/fit-in/448x293/prod01/channel_2/media/migration/staff/Blue-on-white--tojpeg_1495792235526_x4.jpg
    image_alt: "Imperial College London logo"
    text: "Student researcher"
  - title: "Supervisor"
    text: "[Dr James McGinty](https://www.imperial.ac.uk/people/james.mcginty) at Imperial College London"
  - title: "Responsibilities"
    text: "Driving and delivering the project."

---

## Our Imperial MSci project

The Physics MSci project at Imperial College London is a compulsory part of the integrated Master's degree. My partner and I selected a lab-based project and worked on it for a period of around 10 months. Our deliverables were a literature review, a poster presentation, a viva and a project report.

### What is the field of biophotonics?

Biophotonics means using light to measure or inspect biological samples. One example of this is microscopy of cells, tissues and embryos.

### What is Optical Projection Tomography (OPT)?

Different optical techniques are suited for different applications, for example how large the sample is, your acquisiton time, your mode of contrast etc. Traditionally, large 3D biological samples can only be imaged by cutting it up and imaging each slice sequentially, which is time consuming and destroys the sample. OPT is the optical analogue of X-ray Computed Tomography and images sample through a complete rotation. This is particularly useful for developmental biologists who want to study millimetre sized samples such as mouse and zebrafish embryos.

[Read more here!]({% post_url 2023-07-25-opt-summary %})

## What we did

Our project was open-ended from the start. In collaboration with our project supervisor, we had to choose ambitious goals that were possible within our timeframe. We completed the following

* Built, aligned and tested an OPT system that works in fluorescence and transmission
* Optically characterised the system's depth of field and spatially varying modulation transfer function (MTF)
* Applied our system to image phantoms for testing and also a biologically relevant mouse-embryo
* Designed and tested a novel integration of LED microscopy with OPT

We managed to develop a reliable alignment protocol that ensured the rotation axis of the sample was perpendicular to the optical axis.

## Skills developed

**Physics**: understanding of concepts in optics such as depth of field, modulation transfer function, Fourier optics.

**Mathematics**: Radon transform and inverse Radon transform for tomography, an appreciation for Compressive sensing

**Hardware**: System integration of Charge Coupled Device (CCD) with mechanical rotation stage, acquisiton software and LED matrix with Arduino

**Software**: GPU acceleration of reconstruction, image data analysis and acquisition

**Tools**: ImageJ, Python (NumPy, SciPy, Matplotlib, Astra Toolbox), Micromanager, C++ for Arduino

## References

James Sharpe et al. , Optical Projection Tomography as a Tool for 3D Microscopy and Gene Expression Studies. Science 296, 541-545(2002). DOI:10.1126/science.1068206