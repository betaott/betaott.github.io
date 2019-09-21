---
layout: post
title: What is ABR or Adaptive BitRate streaming?
description: Let's understand what is ABR video streaming and how is it different
  from VBR and CBR
category: knowledge
tags:
- vbr
- cbr
- abr
- ott

---
**ABR stands for Adaptive Bit-Rate streaming and it broadly describes the process by which the quality and bitrate of video and audio are adaptively varied to ensure smooth delivery over the internet.**

It is very different from how CBR and VBR operate and an understanding of ABR will make the concepts of video streaming easy to understand.

<br>

## **Why do we need ABR?**

To understand the need for ABR, we first have to recognize that **internet streaming is best-effort**. There are no absolute guarantees on the speed/bandwidth, efficiency, error resilience of streaming over the internet.

This is different from television provided to your set-top-boxes over a cable network which is a managed network. These have guarantees on up-time and it is very rare to see outages and drastic changes in the video quality. If you have bought an HD 1080p subscription to Fox News, then you will see HD 1080p - that's a guarantee.

However, when video is streamed over the internet, things are very different. Why?

Okay, let's assume your house has a 10 mbps internet connection.

Your TV is connected directly to your router using a Cat 5 cable. You have three mobile phones and two tablets also connected to the same internet connection and your kids are using the internet for their homework!

Think of all the devices connecting to the same internet connection at the same time and how much of the bandwidth they are consuming.

Now, you sit down to watch your favorite show and it is possible that your TV's player perceives a 3 mbps bandwidth and uses that to play the show. 10 minutes into your show, your wife decides to open Youtube on her iPad and switches on her favorite show.

**Now what?**

The available bandwidth to your TV drops - perhaps to 2 mbps. Can your TV cope with this sudden change in bandwidth? It jumped from 3 mbps to 2 mbps - a 33% drop!

Now comes the all-important question - **what is your TV downloading, at what bitrate, and at what quality?** If you had a single rendition of the movie, which one would it be?

Let's flip the question around and ask the content provider which bitrate will he encode at to satisfy all the bandwidths at all the different houses?

**It is an impossible proposition - to provide a single rendition or encode of a video that satisfies every bandwidth requirement and restriction for all your users.**

<br>

## **Enter ABR -- tadah!**

From the principles of ABR, the input video has multiple renditions - at different bitrates, resolutions, and frame-rates using different codecs (& profiles) to satisfy a galaxy of bandwidth conditions, screen-sizes, and devices.

Given a source video, the first thing is to encode it at several different **profiles or renditions** and this constitutes a **bitrate ladder.** 

Example, you might encode a video at the following profiles. 

1. 1080p 5.0 mbps
2. 720p 4.0 mbps
3. 640p 3.2 mbps
4. 480p 2.0 mbps
5. 270p 1 mbps

You are free to choose any codec, bitrate, resolution, codec resolution, or frame-rate that you'd like, but you need to be cautious while making your choices. 

For example, if you are streaming to a part of the world where 99% of the population cannot get a bandwidth greater than 2 mbps, then it is a waste of time, money, and storage space to encode at bit rates higher than 2 mbps - correct?

After choosing a bitrate ladder and encoding at those profiles, you package the videos and provide it to the players (end user) using a manifest or playlist using a streaming protocol such as DASH, HLS, HDS, MSS, etc.

Packaging refers to the act of breaking up a video into small segments or chunks so that each of these pieces can be individually requested and delivered to the players -- instead of downloading the entire movie in one go. 

The player then understands how 

![](/uploads/Adaptive_streaming_overview_bit_rates_2011_07_28.png)<center> Image credit: By Daseddon - Own work, CC BY-SA 3.0 </center>