---
layout: post
title: "Continuing Exploration of Fish Movement: A Shift to Polar Coordinates"
date: 2024-10-27 04:45:01
categories: analysis
tags: [fish, movement, graph, bell-curve, simulation]
thumbnail: /blog/assets/241019_bell_curve_fish.png
---

This post continues from my [last discussion](/blog/analysis/2024/10/19/fish-acceleration-graph.html). Previously, I analyzed acceleration in Cartesian coordinates; however, I had a thought—why not switch to polar coordinates? It seems more intuitive for modeling fish movements, where theta represents heading direction and r represents speed.

## Transition to Polar Coordinates and Initial Findings
I converted the acceleration data into polar coordinates. Below are the acceleration graphs for r (speed) and theta (direction), which interestingly continue to follow a Gaussian distribution.

![Bell Curve of Fish Speeds in Polar](/blog/assets/241027_acceleration_polar_bell.png)

## Speed Distribution - Log Transformation and Skewness
In the fish simulation, I generated random values from the probability density function to updated acceleraton. However, a critical observation was that speed (R) must always be greater than zero. This led me to study the distribution of R more closely.

As anticipated, the distribution resembles a Gaussian but, naturally, cannot go below zero. To simplify modeling, I transformed R using the logarithm, enabling me to fit a left-skewed normal distribution. Here’s a histogram illustrating this:

![R analysis](/blog/assets/241027_r_analysis.png)

## Simulation Time!
So now I got two distributions: Gaussian distribution for the acceleration (delta_R), left-skewed normal distribution for speed (R). 

Next, I wondered: if all these delta_R data (changes in R) come from a Gaussian, does R play along as expected? I set up a simulation to test this out, constantly generating and applying delta_R values to see what happens. Here are the results:

![sim result](/blog/assets/241027_sim_result.png)

Surprisingly, while the overall shape was somewhat similar to the expected model, it was noticeably shifted (regardless of initial R value). This indicates that while our model is on the right track, some adjustments may still be necessary to align the simulation more closely with observed behaviors.

This exploration highlights the iterative nature of scientific modeling and simulation—each step brings new insights and questions. Further adjustments and analyses will be necessary to refine my understanding of fish movement and ensure the models accurately reflect the collected dataset.