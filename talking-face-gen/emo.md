---
title: EMO Review
layout: page
parent: Talking Face Generation
nav_order: 2
---

# Summary

[EMO] aims at tackling the challenge of generating expressive and lifelike (as real
as possible) talking head videos by using a diffusion model that goes directly from
audio to video without needing any intermediate 3D representations.
They claim that the traditional techniques often fail to capture the full spectrum
of human expressions and uniqueness of individual styles, which mainting identity
throughout the generated video.

Core Contributions:
1. Train a model directly on audio and a single image to generate a video with
expressions that are faithful to the audio signal and the identity is preserved.
  * Adding audio to expressions mapping through a diffusion model is not easy as
  it's an uncertain mapping, which can introduce jitters or instability in the
  generated output. They have introduced a speed and face region controller as
  hyperparameters to make the generated output stable.
  * Their approach does not require any intermediate 3D representations for the
  face, which means the mapping is implicit and a control mechanism to modify
  expressions, head pose or eye gaze is not possible.
2. They use the approach mentioned in ReferenceNet and enhanced it to ensure that
the identity in the single reference image provided stays consistent throughout
the video.
3. They create an audio-visual dataset, which is over 250 hours of footage and more
than 150 million images.
  * This expansive dataset encompasses a wide range of content, including speeches,
  film and television clips, and singing performances, and covers multiple languages
  such as Chinese and English. The rich variety of speaking and singing videos ensures
  that our training material captures a broad spectrum of human expressions and
  vocal styles, providing a solid foundation for the development of EMO.
  * SOTA across multiple metrics such as FID, SyncNet, F-SIM, and FVD. In addition
  to quantitative assessments, we also carried out a comprehensive user study and
  qualitative evaluations.


# Main Components

...


----

[EMO]: https://humanaigc.github.io/emote-portrait-alive/