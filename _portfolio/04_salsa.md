---
title: "WIP (Active): Salsa App"
excerpt: "Full stack web/ mobile development using Flutter and Firebase."
header:
  teaser: /files/salsa/phone.png
sidebar:
  - title: "Timeframe"
  - text: "Dec 2024-ongoing"

mathjax: true
---

![Salsa](/files/salsa/phone.png)

I made a web/ mobile application for keeping track of Salsa practices, as I found it quite difficult just using the photos app on the phone. This was also a good opportunity for me to learn some web/ mobile development.

Flutter uses Dart, a language that isn't so similar to Python which I had to learn. Firebase on the other hand is known as a 'Backend as a Service,' which has a generous free tier and shortens development time significantly.

## Computer vision

For my app, I wanted to create an automatic way of time-segmenting individual moves. My idea was to effectively extract the 1-beat, based on the foot steps. (An alternative solution was to to look at the audio spectrogram to extract the beat from sound features.)

The reason this is tricky is 3 fold

1.  The camera is not still
2.  There is occlusion
3.  There is ambiguity in the location of the joints in 3D space.

I used a pose detection model to estimate the joints of the people in the frame. I then chose the two most salient people in the frame.

![alt text](/files/salsa/pose.png)

I then plot the time series. Here I track the keypoints in the x direction. My hypothesis was that by taking a Fourier transform of the time series for the leg keypoints, I would be able to extract the salsa beat, however, this turned out to be noisy, as cross bodies and position switches meant that the signal strength is lowered.

![alt text](/files/salsa/features.png)

The difficulty in obtaining the rhythm from movement has made me consider other approaches to the problem such as body fitting, which is state of the art! This way I'm tackling the general problem head on.

![alt text](/files/salsa/body_fitting.png)

My ultimate goal is to create a database of dance moves so I can practice from.

## Updates

- Dec 2024: Learning firebase and flutter from scratch
- Jan 2025: frontend, backend linked. Routine-based view is available. App is deployed and live!
- Feb 2025: improving the UX via incorporating a move-based view. Discovering issues on web on iPhones...

## Skills developed

**Programming**: Firebase, Flutter, App development, UI/ UX

**Computer vision**: Human pose estimation, signal processing
