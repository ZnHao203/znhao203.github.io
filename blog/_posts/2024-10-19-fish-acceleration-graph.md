---
layout: post
title: "Analyzing Fish Movement: From Data to Bell Curve"
date: 2024-10-19 11:40:01
categories: analysis
tags: [fish, movement, graph, bell-curve]
thumbnail: /blog/assets/241019_bell_curve_fish.png
---

In this post, I’ll quickly walk through how I analyzed the swimming patterns of my fish and plotted a bell curve of their acceleration distribution.

## Steps
First, I used a webcam to capture pictures of the fish tank every second. Then, I used OpenCV to identify the position of the fish based on its color. To keep things simple, I used the center of the bounding rectangle (created by color detection) as the fish's position. From there, I calculated the velocity and acceleration in both the x and y directions.

## Result
The acceleration analysis showed that the fish’s movement followed a bell curve. Below is the graph I generated from a set of images—about 30 minutes of footage, with one picture taken per second.

![Bell Curve of Fish Speeds](/blog/assets/241019_bell_curve_fish.png)

Though I will need to do further analysis and integrate this data into the larger picture of fish movements, this is a nice temporary result to share.