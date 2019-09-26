---
layout: post
title: How does HLS video streaming work?
description: 'Learn how the hugely popular HLS (HTTP Live Streaming) is defined, how
  it works, which players can play HLS streams, and popular use cases for HLS.  '
category: knowledge
tags:
- hls
- video streaming
- ott

---
## The need for HLS

I've written about  ABR or adaptive bitrate video streaming \]({% post_url 2019-09-22-what-is-abr-or-adaptive-bitrate-streaming.md %}) in the past and discussed in detail what ABR is used for. To recap, adaptive bitrate video delivery is a way of delivering video where the player or client detects the available bandwidth and then modulates/adjusts the quality of the video stream between multiple bitrates and/or resolutions (typically referred to as a "bitrate ladder")