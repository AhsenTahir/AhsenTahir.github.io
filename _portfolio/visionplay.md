---
title: "VisionPlay — multi-object tracking in broadcast sports footage"
excerpt: "Fine-tuned YOLO + ByteTrack for player and ball tracking, with optical-flow camera-motion correction before pixel-to-field coordinate mapping.<br/><img src='/images/projects/vision-play.jpg'>"
collection: portfolio
---

Real-time football match analysis from broadcast footage. A fine-tuned YOLO detector plus ByteTrack handles player, goalkeeper, and ball tracking; k-means over jersey colour assigns teams.

The interesting part is the camera: broadcast footage pans and zooms constantly, so raw pixel coordinates are meaningless as field positions. Optical flow estimates and corrects camera motion before the pixel-to-field homography, which is what makes the derived per-player possession, speed, and distance statistics trustworthy.

**Stack:** YOLO, ByteTrack, OpenCV, k-means, Python

[GitHub](https://github.com/AhsenTahir/VisionPlay-Next-Gen-Sports-Analytics-)
