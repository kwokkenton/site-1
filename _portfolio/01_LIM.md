---
title: "3D Hyperspectral Point clouds: Poster at London Imaging Meeting"
excerpt: "Presenting my work in hyperspectral computer vision."
header:
  image: /files/lim/heading.png
  teaser: /files/lim/conference.png
sidebar:
  - title: "Role"
    image: /files/lim/livingoptics_logo.jpg
    image_alt: "Living Optics logo"
    text: "Field Applications Engineer"

  - title: "Timeframe"
  - text: "Mar-Jun 2024"

  - title: "Responsibilities"
    text: "Planning, executing and presenting the project."

mathjax: true
---

## A wild idea come true! Also my first conference presentation

🗣️Conferences allow research-oriented scientists or engineers to learn about the latest developments in a specific subfield. They operate at a quicker pace than journal submissions and the in-person element allows for a much natural discussion of ideas. Doing a technical presentation can also help to generate good PR/ Marketing, especially if you’re a small startup!

🌆The London Imaging Meeting (LIM) is a space for researchers and industry professionals to discuss imaging science research and technology. It presents new papers in different areas of imaging each year, focused especially on topics that lead and seed future research directions.

💭On behalf of the company, I talked about my work on 3D hyperspectral point clouds (basically a collection of points in 3D space) and how our technology can create these objects much quicker than other commercial products.

![Conference](/files/lim/conference.png)

## What do Living Optics do?

As of the time of writing, [Living Optics](https://www.livingoptics.com/) is an early stage startup aiming democratise spectral imaging by manufacturing a low-cost, easy-to-use hyperpsectral camera for computer vision developers.

As an applications engineer, I use my training in physics and computer vision to explore new ways developers can use our camera. I directly train and support our customers and run research projects to develop new applications.

## What I did

Photogrammetry is the technique of obtaining 3D
information through the process of recording and
incorporating images. The RGB cameras that are often
used in photogrammetry, as with the human eye, can only
capture a fraction of the richness of information in the
natural world as only 3 bands of data can be extracted. In
contrast, hyperspectral imaging provides fine-grained
radiance information over a certain spectral range,
enabling precise quantification of material properties.

While multispectral photogrammetry has found
applications in agriculture, hyperspectral
photogrammetry has been limited in its uptake due to its
high cost, low ease of use and long acquisition times [1].
The possibility of encountering motion artifacts in typical
spatial or spectral scanning systems exacerbates this
problem.

![The premise](/files/lim/problem.png)

We propose a method of collecting 3D hyperspectral
data using a snapshot imager, that allows quick
generation of point clouds. We anticipate applications in
robotics, surveying, inspection and precision agriculture in
tasks such as plant health analysis and yield estimation.

Photogrammetric reconstruction was performed
using the open-sourced Meshroom package [2]. The
software takes in a series of photos and for every image, it
outputs the camera’s pose in world-coordinates and a
dense depth-map of the scene. Spectral points were
back-projected into 3D coordinates and visualised using Open3D by applying rigid transformations and inverse projective geometry.

![alt text](/files/lim/sfm.png)

Using a spectral band ratio allows you to easily segment out the organic material compared to the inorganic material (due to the presence of cholorophyll). The green leaves also have slightly higher NDVI than the strawberry flesh.

### Sidenotes

🍎Other interesting happenings

- A company unveiled their smartphone camera module on panoramic imaging without panning, which was pretty cool!
- There was a super interesting talk on underwater imaging... how researchers are attempting
- It was the first time being in the Institute of Physics, which was a modern-fitted space inside typical Georgian terraced housing
- Although there were mainly technical talks, the organisers invited a seasoned photographer to share some of his thoughts on taking good photos. PS. He despises the rule of thirds.

🤘🏼In case you are also a young professional working in industry, I think joining conferences are a good way to learn about things outside your day-to-day and to meet interesting people. SIGGRAPH have a really good [“Get your boss on-board”](https://s2024.siggraph.org/ask-your-boss/) template article which you can use to persuade whoever is in charge. In summary, emphasise the value it brings to the company and that it’s also for your personal development. Also remember to give an estimate of the costs.

## Skills developed

- **Computer Vision**: understanding of structure from motion, pinhole camera model, lens distortions, point clouds.
- **Spectral Imaging**: band ratios, NDVI
- **Tools**: Meshroom for Structure from Motion, Open3D for visualisation

## Related work

- [1] G. J. Edelman and M. C. Aalders, ‘Photogrammetry Using
  Visible, Infrared, Hyperspectral and Thermal Imaging of
  Crime Scenes’, Forensic Science International, 292 (2018)
- [2] AliceVision, Meshroom: A 3D reconstruction software,
  GitHub (2018).
- [3] Rouse, J. W et al., “Monitoring vegetation systems in the
  great plains with ERTS,” NASA. Goddard Space Flight Center
  3d ERTS-1 Symp. 1(A) (1974).
