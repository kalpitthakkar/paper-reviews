---
title: VASA-1 Review
layout: page
parent: Talking Face Generation
nav_order: 2
---

# Summary

[VASA-1] is a premiere model from Microsoft Research Asia, that is claimed to be "able to produce lip movements that are exquisitely synchronized with the audio, but also capturing a large spectrum of facial nuances and natural head motions that contribute to the perception of authenticity and liveliness."

Core contributions:
1. Diffusion-based model that works in face latent space
  * Generates realistic __facial dynamics__ and __head movements__. Facial dynamics include lip motion, (non-lip) expression, eye gaze and blinking, etc.
  * Learns a disentangled expressive face latent space using videos. Facial dynamics are learned as a single latent variable, whose probability distribution is modeled.
  * They incorporate conditional generation as well, with conditions such as __main gaze direction__, __head distance (from camera)__ and __emotion offset__.
2. Their latent space has very good disentanglement for facial dynamics, identity, head pose and 3D appearance.
  * A good, expressive dataset is required for this: they used 46 subjects from VoxCeleb2 and collected a dataset of 32 1-min clips of 17 individuals that has considerably more diverse speaking styles compared to VoxCeleb2.
  * They train a Diffusion Transformer (encoder - decoder) that takes frames from face video as input and learns the motion distribution via latents. Classifier-free Guidance is used to train it with conditioning signals mentioned above.
  * To prove their disentanglement power, they keep one of the axes constant and vary the others: for example, keeping the identity constant but changing the head motion or emotion offsets shows that the identity is not degraded.
3. High-quality output generation (512 x 512) at upto 40 FPS, with realistic facial and head dynamics in the generated video.


# Main Components

WIP



----

[VASA-1]: https://www.microsoft.com/en-us/research/project/vasa-1/