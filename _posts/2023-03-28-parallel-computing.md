---
toc: true
layout: post
description: Includes Important Notes about Algorithm Complexity and managing high volumes of complexity
categories: [markdown, Comp Sci]
title: Parallel Computing + Hashmaps Notes
permalink: /notes/parallel
comments: true
---

# Class Notes - Parallel Computing

top -H gives a list of processes! I've run this on Linux machines before. You want to run this on a terminal. There is a #TH in Mac and/or the total number of threads at the top. I think number of threads is also available via Windows Task Manager.

When the code affecting the images is run, there is a img.putdata([grey_pixel(pixel) for pixel in image['numpy']]). This is a for loop in one line, with brackets for the list. There is a list comprehension hacks exercise (I'll have to use the W3Schools Python interpreter for that). You put the list of the for loop into the list.

**Sequential Processing** example: Each image is processed **one at a time**. In order to see this more clearly, the class increased the baseWidth to 2000 pixels. Since it took half a minute for each set of images to render on Lily's computer, it was more obvious that sequential processing was occurring.

**Parallel Processing**: Each of the images are processed simultaneously. Mr. Yeung's execution took 43.9 seconds rather than 48 seconds. This was largely dependent on the threads. Mr. Yeung observed 110 threads initially/during sequential processing, but 113 threads while the parallel processing was occurring. Mr. Yeung also noted that computers can max out their threads and parallel processing would not be too different. In my opinion, parallel computing should be faster if computing resources are not being strained by other processes

Chinmay asked if it was possible to apply multiple threads to the same loop (iteration operation). Mr. Yeung responded that it is not possible to run multiple threads on one loop, but it is possible to run multiple threads on multiple loops. However, setting up multiple loops would be impractical/inefficient 
