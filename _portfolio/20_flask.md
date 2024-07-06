---
title: "Pet project- Memento"
excerpt: "Face recognition, networks and web app development."
header:
  teaser: files/portfolio/memento_result.png

---
## What is Memento?

![Happiness](https://images.unsplash.com/photo-1580640611343-3f53b12a5b1d?q=80&w=1074&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D)

People are forgetful. On the hedonic treadmill of life, we often forget how lucky and fortunate we are. This sense of discontent and inadequacy which is made worse by constant comparison on social media.

Numerous [studies](https://www.health.harvard.edu/healthbeat/giving-thanks-can-make-you-happier) show that if we remember to give thanks and display gratitude, we will become happier.

I wanted to make a solution to hedonic adaptation, originally thinking of a hardware solution of a photo frame that selectively. However, this seemed to coincide with a standard digital photo frame product (that you can buy online), or even the default photos app on the iPhone or Google photos, which makes video collages to take you on a trip down memory lane.

After a couple pivots I thought simply showing personal relationships could make for a viable demo.

## What did I do?

Log in page to upload images

![Memento result page](/files/portfolio/memento.png)

Result page (generated after a few seconds)

![Memento result page](/files/portfolio/memento_result.png)

### Tools

- The usual Python DS stack: NumPy, Matplotlib
- [Face-recognition](https://github.com/ageitgey/face_recognition) as the ML backend for doing the face extraction and recognition.
- [NetworkX](https://networkx.org/) for generating the plots
- [Flask](https://flask.palletsprojects.com/en/3.0.x/) as the web backend.
- [Docker](https://www.docker.com/) for containerising and deploying the app.
- [MongoDB](https://www.mongodb.com/) NoSQL database experimented on but not used in deployment.