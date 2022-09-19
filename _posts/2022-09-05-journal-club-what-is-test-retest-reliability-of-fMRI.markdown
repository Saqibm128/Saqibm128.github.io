---
title:  "What is test-retest reliability of fMRI?"
date:   2022-09-05 15:07:21 -0400
categories: postbac research journalclub
---

I want to go and work through various articles that are inspiring or cool or interesting. One of the cooler articles which helped when I was first getting started on MRI work was this meta-analysis article:
* Link to the article. https://pubmed.ncbi.nlm.nih.gov/32489141/

As of the time of this blog post, this article has been cited more than 300 times. It's a form of meta-analysis that attempted to use a metric they call "intraclass correlation coefficient".

# What is ICC?

What exactly is the intraclass correlation coefficient (ICC)? [Wikipedia](https://en.wikipedia.org/wiki/Intraclass_correlation) describes it as "a descriptive statistic that can be used when quantitative measurements are made on units that are organized into groups." In the context of this paper, it's used to measure whether studies are necessarily correlated in their findings i.e. if they agree with each other.

An ICC must be greater than 0 to better than useless (i.e. a study will probably agree with the initial results we came up with if we repeat it.) To be really ueful for clincial or psychological standard, this article states in the appendix than an ICC of greater than 0.8 is required.

# Power analysis breaks my heart
An initial power analysis is done with simulated studies in figure 1 of this article. I think perhaps this figure is a bit hard to read but illustrates a few ideas. First, fMRI studies on human brains have to deal with human variability; there is sufficient variability in human brains that the same task might elicit different responses in different peoples brains. In some cases, it may not elicit a response at all in the expected brain area for a few folks! This is reflected by the "ICC of Associated Phenotype" title. 

The gradation of the graph is a measurement of the ICC of the study itself. Ideally, we want a study to fall in the light gray area (ICC > 0.75). Depending on the effect size (how big a change shows up in the BOLD response and other derived measures), we may need up to hundreds of subjects to get a useful response. 

This is shocking, to say the least; individual studies often use less than 50 subjects total, and some are published with as few as 20. As part of my lab, some disorders are fairly rare or are hard to properly adjudicate patients that trying to find 20 subjects is rather difficult.

# Meta-analysis to beat all other meta-analyses
The next part of the paper uses a meta-analysis to try to measure the ICC of various effects that were reported in other papers. The meta-analysis is almost like a meta-analysis of various meta-analyses. Results are shown in figure 2. What's striking is not only that various studies had ICCs which could range closer to close to useless, but that error bounds for many of the estimates indicate that many effects that had a mean in the "good" range might have had their actual ICC in the poor range.

A final analyses was done using publicly available HCP data. The HCP is a large-scale open-access dataset of thousands of young subjects' MRI scans. The scans included 7 tasks. 

# HCP and Dunnedin study
The authors ran a data analysis on this against the Dunedin study, which was a similar study of 1000 subjects. There is a bit of an age discrepancy (HCP subjects are in their 20s or 30s, while Dunnedin subjects may be closer to 45), but it should probably not be too much of an issue.

45 of the HCP subjects were evaluated for the same task twice using the same scanner for 7 tasks. Similarly 20 participants in the Dunedin study were scanned twice on the same scanner a few months apart. While the author's point out they used what was publicly available, this may raise possible issues of selection bias.

Analyses is detailed in the paper and seems fairly standard. Regardless, ICC for the HCP subjects the researchers selected ended up being only 0.251, which is nearly useless. ICC for Dunnedin is not much better, around 0.309.

As a final analysis, the researchers also did this ICC work using the sMRI data instead of the fMRI. ICC remained around 0.9, which is to be expected. I might suggest that it may have been more interesting to report ICC between different scanners for the same patients, if such data exists in the HCP or Dunnedin.


# Conclusions
fMRI studies are not useless, with many effects from the meta-analyses having mean ICCs in the 0.7 to 1 range (good to excellent). However, there are issues in many fMRI designs. sMRI datasets (surface area, brain volume) on the same scanners seems to have the best ICCs.

The authors go through a few issues that may help increase ICC.
* It's important to pick a priori areas of the brain first instead of looking for an area and then deciding the effect size of the effect based on it.