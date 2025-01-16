---
title: "Computational biophotonics- imaging mouse embryos in 3D using OPT (MSci Thesis)"
excerpt: "Doing benchtop optics, programming and analysis for biology!"
header:
  image: files/opt/embryo.jpg
  teaser: files/opt/embryo.jpg
sidebar:
  - title: "Role"
    image: /files/opt/imperial-600.png
    image_alt: "Imperial College London logo"
    text: "Student researcher"
  - title: "Timeframe"
  - text: "Sep 2022-Apr 2023"
  - title: "Supervisor"
    text: "[Dr James McGinty](https://www.imperial.ac.uk/people/james.mcginty) at Imperial College London"
  - title: "Responsibilities"
    text: "Driving and delivering the project."
---

## Our Imperial MSci project

The Physics MSci project at Imperial College London is a compulsory part of the integrated Master's degree. My partner and I selected a lab-based project and worked on it for a period of around 10 months. Our deliverables were a literature review, a poster presentation, a viva and a project report.

![alt text](/files/opt/opt.png)

### What is the field of biophotonics?

Biophotonics means using light to measure or inspect biological samples. One example of this is microscopy of cells, tissues and embryos.

## Who cares?

Developmental biologists are people who are interested in studying how organisms grow. They may study embryos, larvae and even whole organisms. As you may well know, scientists cannot directly perform these experiments on humans due to certain ethical reasons (imagine the uproar!). This is one reason why developmental biologists result to studying ‘model organisms’ such as mice and their embryos, that are structurally similar to humans.

There is a need to image these millimetre-sized specimens. The traditional way to do this has been cutting up the embryo into hundreds of slices, imaging them sequentially and computationally stitching them together. However, this is extremely time-consuming. Optical Projection Tomography (OPT) is a relatively new volumetric bioimaging technique that does this non-invasively and is the optical analogue of X-ray CT. A few hundred images of the sample are taken, as it undergoes a complete rotation (unlike medical CT scans when the source and detector rotate instead). The stack of images is then processed using a computer with what is called the filtered backprojection algorithm to do a slice-by-slice reconstruction of your sample— allowing you to look inside it without cutting it up. This is done using visible light because biologists know how to label specific proteins or genetic material with either precipitates that attenuate light or fluorescent markers that emit light when excited with photons that correspond to its energy gap. These markers do not exist with other similar techniques such as MRI or X-ray CT.

![alt text](/files/opt/FBP.png)

Biological tissue is usually milky in appearance due to the scattering of light. However, one requirement of OPT is that samples have to be see-through. Thankfully, a range of chemical techniques have been developed to perform optical clearing for us.

### What we did

![alt text](/files/opt/opt_setup.png)

We constructed an OPT setup (think screws and Allen keys), wrote the image processing scripts (lots of debugging) and applied it to image an optically cleared mouse embryo (with gloves because the clearing substance is somewhat toxic).

![bead resolution](/files/opt/resolution.png)

As physicists, we wanted to determine the limits of imaging performance. One such measure is image resolution, which is the minimum distance two signals can be separated for them to still be distinguished. The resolution is limited by diffraction from the aperture in the lens, which is best at large aperture sizes. As we needed the whole sample to be in focus when imaged, we also wanted to have a large depth of field, which is favoured with small aperture sizes. This unfortunately is the trade-off in OPT! We took images of known physical targets (a sharp knife edge and a fluorescent sample bead sample) to quantify this effect so OPT users can know the optimum aperture size for their sample.

![alt text](/files/opt/RI.png)

In addition, we also prototyped a new system that uses an LED matrix as illumination. We discovered that by illuminating successive halves of the LED and taking images over a complete rotation, we can reconstruct the entire 3D refractive index of the sample! This is pretty exciting as existing methods that do this are complicated and expensive. It can be applied to label-free imaging of zebrafish, which developmental biologists know and love. We enjoyed this project as it’s a manifestation of how physical principles, experimentation and computation all have a role in understanding complex biology— one embryo at a time.

![GIF of mouse embryo imaged](/files/opt/mouse.gif)

_3D render of the mouse embryo we imaged._

Succinctly, we

- Built, aligned and tested an OPT system that works in fluorescence and transmission
- Optically characterised the system's depth of field and spatially varying modulation transfer function (MTF)
- Applied our system to image phantoms for testing and also a biologically relevant mouse-embryo
- Accelerated tomographic reconstruction by 20x using ASTRA toolbox in Python with a GPU
- Demonstrated, for the first time, volumetric phase imaging with OPT using diﬀerential phase contrast (dpc-OPT) without interferometry

We managed to develop a reliable alignment protocol that ensured the rotation axis of the sample was perpendicular to the optical axis.

## Skills developed

**Physics**: understanding of concepts in optics such as depth of field, modulation transfer function, Fourier optics.

**Mathematics**: Radon transform and inverse Radon transform for tomography, an appreciation for Compressive sensing

**Hardware**: System integration of Charge Coupled Device (CCD) with mechanical rotation stage, acquisiton software and LED matrix with Arduino

**Software**: GPU acceleration of reconstruction, image data analysis and acquisition

**Tools**: ImageJ, Python (NumPy, SciPy, Matplotlib, Astra Toolbox), Micromanager, C++ for Arduino

## References

James Sharpe et al. , Optical Projection Tomography as a Tool for 3D Microscopy and Gene Expression Studies. Science 296, 541-545(2002). DOI:10.1126/science.1068206
