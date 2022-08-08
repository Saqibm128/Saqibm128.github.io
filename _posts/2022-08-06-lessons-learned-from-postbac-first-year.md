---
layout: post
title:  "Lessons learned from my first year as a postbac"
categories: postbac research
---
# Introduction

As I complete my first year of my postbac, I thought it might be nice to go and make a list of lessons that I've learned during my time here at the NIH. A bit of background is probably necessary to fully understand my perspective.

## Background

I attempted to apply for graduate school and applied to schools during the 2021 application cycle. I got rejected from all schools except 1, who decided was no longer a good fit, as the projects I were interested in had lost funding. I realized I failed due to a number of circumstances and that perspective at the NIH could be useful to help narrow down exactly what I needed to focus on. I learned a lot from my time here.

# Lessons
## Technical

1. Preprocessing MRI is hard.
* There is no right way to process this kind of data, but there sure are a ton of wrong ways to process it. In particular, double checking the data is imperative at all stages of processing. I lost a month of work to having failed to catch a simple alignment issue with fMRI data for a graph analysis workflow and had to start all over from the beginning.
* Different MRI sequences require vastly different preprocessing techniques.
* Most of these MRI preprocessing pipelines use up a ridiculous amount of compute power taking hours to literal days to complete.
2. Different scanners and devices wreak havoc with statistical analyses.
* In a way, this is the crux of the research problem I am attempting to tackle.
* Of particular note, some diseases, such as Parkinsons (PD) are ridiculously heterogenous.
3. Balancing data can help solve for some issues in modeling and machine learning but isn't always necessary.
* Sometimes trying to stratify by all the different combinations of labels for a scan can get rather involved and limit your training set.
* Using balanced metrics or using balanced weighting may be far better.


## Personal Issues
* Working from home kills productivity
Its far too easy to access your phone and the social pressures of working are lessoned when theres noone else to judge you while you waste time working.
* I need to be better at protecting an early bed time.
Postbacs are usually college kids who never developed adult habits like sleeping on a regular schedule. Sleeping late is fairly immature.
* I have a tendency to see the negative in situations, which leads me to spiral.
It's way to easy for me to get lost in failing results and my productivity as a result suffers.
* I need to learn to accept when a scientific theory or some proposed methodology I am suggesting might fail.
