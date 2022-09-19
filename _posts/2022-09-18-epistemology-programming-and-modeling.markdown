---
title:  "Epistemological responsibility, programming, and modeling, oh my!"
date:   2022-09-18 00:00:00 -0400
categories: research rant

---

![Picture of tangled wires symbolizing spaghetti code](assets/spaghetti-code-title.jpg "Photo Cred: https://exceptionnotfound.net/spaghetti-code-the-daily-software-anti-pattern/")

A colleague of mine, from when I was a software engineer, shared a blog post about the pitfalls of dealing with old codebases. The article was describing a case study of a system of spaghetti code that was cobbled together through an arcane set of competing dependencies, insane design patterns, and everything else that one generally should not do when programming a large scale system. The blog post was asking, or rather, begging fellow developers for advice around trying to handle the codebase. The author implied that their coworkers had been lax in continuing to allow the codebase to continue to work as is.

Other programmers poured in, providing their own takes and their own experiences. The programmers who answered the plea for help suggested that the code and the logic the code implemented should be respected. Although the design principles were horrid, the code was still functioning and moving $20 million in revenue each year. More importantly, it had properly modeled the real world. Though carefully reading the actual code itself was painful, there were important snippets hidden in the aweful software that handled exceptions to the rules and weird business scenarios in the real world. It would be completely unlikely a new coding team could properly replicate all of the correct logic if they made a new product from scratch.

The best advice was towards refactoring the code bit by bit, in a modular fashion, with tests to make sure that changing one part of the whole system at a time didn't destroy the behavior of the whole system. It would be best to try to replicate the business logic for each part, but never attempt to completely destroy the old code base and start anew. (See [Joel Spolsky's classic take for another case study](https://www.joelonsoftware.com/2000/04/06/things-you-should-never-do-part-i/))

---

![Axial slice of brain MRI](assets/generic-brain-scan.jpg "Photo Cred: https://www.kenhub.com/en/library/anatomy/normal-brain-mri")

This led me to consider my own work with MRI. I recently had been working on aligning fMRI T2 data to sMRI anatomical T1 data. In layman's terms, I was taking what was the video of the brain's activity and matching it towards a higher resolution photo of the brain anatomy. The video is a very blurry and coarse sort of approximation of brain activity; think of 144p YouTube videos from the mid 2000s kind of blurry. It's very hard to figure out where activity in the brain corresponds to which area in the brain, so using the known reference of a high resolution image is useful.

Unfortunately, I was having issues with my alignment process; it appeared that the T2 data refused to align with the T1 data, such that the T2 data's blurry brain was several centimeters above the T1 data's actual brain. For some subjects, this clearly destroyed any sort of real comparison of brain activity, as it was impossible to really tell which brain activation corresponded with which brain location. For other subjects, the T1 scan was only slightly off, so the activity wasn't entirely impossible to interpret.

I spent the better part of last week trying to figure out why the T2 and T1 scans refused to align. Part of me had thought I was spending too much time and perhaps the brain scans would never really align. Nobody else would check this data anyways, so why bother?


---

I think these two seeming disparate problems I just described are unified by a similar fundamental issue.

Epistemology is defined as the study of knowledge, and epistemological responsibility, in a nutshell, is the idea that you should not necessarily mislead others with false knowledge or send them on a journey that will lead to false conclusions. Programming and scientific modeling are the kinds of scientific pursuits that can lead to either real knowledge being found and preserved or to knowledge and the process of managing that knowledge being thrown out. I'd argue that there is potential for great epistemological good or evil with both.

After all, if you think about, if I processed the MRI data wrong, the original raw data still would exists. Someone else could deal with the issue later. Similarly, if someone decided to completely throw away all those hard-won lesssons in business logic from the original code base and make a completely new code base instead of incrementally evolving the code, the old codebase would still exist to refer to if something went wrong. But the process to find what is true, to maintain the correct, would be broken.

The issue is whether we respect the knowledge, the data, and what is actually true. It's a kind of integrity towards understanding the world, in all its complexities, and trying to properly organize it to build a good foundation on.

---

I did eventually end up successfully aligning the MRI data in the end. It was tough, and I had to test a ton of different options on the data. I ended up manually reviewing hundreds of MRI scans repeatedly to confirm which process worked and which didn't. Though this ended up taking much more time to figure out the issue than I expected, I am glad to know I can have trust in the process.