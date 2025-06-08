---
title: "Salseros Web App"
excerpt: "Full stack EdTech web development."
header:
  teaser: /files/salsa/phone.png
sidebar:
  - title: "Role"
  - text: "Dev"
  - title: "Timeframe"
  - text: "Dec 2024-ongoing"

mathjax: true
---

![Salsa](/files/salsa/image.png)

Salsa is an improvised dance and as a leader in salsa (as opposed to a follower), you had to suggest moves whilst basically **improvising** to each song. I went to classes and after attending for a few months, I found it quite difficult to keep track of everything I learnt just using the photos app on the phone.

This was because

- I found it difficult knowing what was in each video file was
- sometimes I wanted to individually isolate each move and practice them
- I wanted to keep track of my progress in learning moves
- I wanted to have something to refer to during class socials
- I also wanted an easy way to share videos with other dancers and have a collected video bank

Deliberate practice is important for improving at anything for beginners. So, I made a web/ mobile application for keeping track of Salsa practices! This was also a good opportunity for me to learn some web/ mobile development.

[Check out the app here!](#link){: .btn .btn--success}

The current application is made using a React frontend, a FastAPI backend and

## Features

Features

- View video during practice
- View captioned moves to learn how to describe what you're doing
- Filter by style, teacher, difficulty to hone in on perfecting the routine
- Add your own moves to share with others

Backend features

- Compression

## Research work

_I originally wanted the app to involve a great deal of computer vision, but it turned out that video-based computer vision still lags a lot behind image-based CV. This has been put on the backburner as I discovered that it wouldn't make sense for an MVP to have all of this. For small datasets, **manual** annotation is still OK._

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

Separately, I thought it would be interesting to see whether vision-language models can interpret the video. Here I provided a video to Gemini to see whether.

![alt text](/files/salsa/gemini.png)

This was the response

```
Certainly! Here's the timestamp breakdown for the salsa moves demonstrated in the video, along with a description of each move:
Timestamp Breakdown:
0:00 Basic move
0:02 inside/ outside turn
0:04 hair brush
0:05 arm flick
0:08 cross body lead
0:10 cross body lead
0:13 arm flick
0:15 cross body lead
0:17 arm flick
0:18 Basic move
0:21 basic move
0:24 the reverse hair brush and dip
Let me know if you need anything else!
```

It gets the more apparent moves correctly, such as arm flicks and dips, however most of the 'basic moves' and 'cross body leads' are hallucinated. I tried better prompt-engineering but the video-language model still does not have enough understanding of salsa to accurately 'describe' the salsa moves. Unfortunately we do not have the ability, nor the dataset, to fine-tune the model.

## Updates and Engineering Log

- Dec 2024: Learning firebase and flutter from scratch
- Jan 2025: frontend, backend linked. Routine-based view is available. App is deployed and live!
- Feb 2025: improving the UX via incorporating a move-based view. Discovering issues on web on iPhones... Investigating computer vision based move annotation.
- May 2025: Scrapped Firebase codebase, rebuilt app using React, FastAPI on a [Hetzner instance](https://www.hetzner.com/cloud).

I originally developed the app using [Flutter](https://flutter.dev/), which is a Dart-based framework for mobile, web and desktop development using a single codebase. Firebase on the other hand is known as a 'Backend as a Service,' which has a generous free tier and shortens development time significantly. After a few months of development, I decided to rebuild the app using React and FastAPI for multiple reasons:

- It was apparent that a mobile app wasn't crucial to the service
- Development in Flutter was very slow
  - There weren't as many libraries and the ones that existed were not that well documented
  - The backend/ frontend separation was not as clear
  - Javascript felt much more intuitive to me and I already knew Python pretty well
  - Using React meant that I had access to the best frontend component ecosystem
- I wanted to learn how to deploy an app on a baremetal server.

I continued using Firebase as the database and bucket service as it did its job pretty well.

- June 2025: Deployed and launched!

## Skills developed

**Programming**: Firebase, Flutter, App development, UI/ UX, FastAPI

**General**: User research, product

**Computer vision**: Human pose estimation, signal processing
