---
layout: default
title: Talking Face Generation
nav_order: 2
has_children: true
---

The task of talking face generation --> generating video of an identity (or identities) talking, given an audio clip (or clips) and an image (or images) of the identity (or identities), ensuring accurate lip-sync and natural emotion + facial dynamics based on the audio signal (or signals).
Add-ons to the base task include:
1. Controls for emotion, head motion and eye gaze
2. Audio-related controls: autodubbing and lip-syncing on arbitrary audio

Other 3D vision related controls like distance from camera, generated video resolution, etc. are also possible.

For a talking face generation system to be ideal (with controllable generation), the main requirements are:
1. Disentangled space (latent or otherwise) for representation of identity, appearance, facial dynamics (lip, non-lip and eye movements) and head pose. The control in generation and it's realism is directly proportional to the degree of disentanglement.
2. Identity-preserving: this is directly related to the disentanglement point - when using different audio signals, emotions or head poses, the identity should not be affected in the generated video.
3. Expressiveness of the talking face in the generated video: realism is directly proportional to the expressiveness, unless it's so extreme it becomes uncanny.
4. Perceptual quality and output resolution of the generated video: realism is proportional to the perceptual quality (as evaluated by a human) and output resolution.

For all papers, we will focus on which of these four aspects they're good at and consider learning why it is so in order to apply those principles in our models.

Papers:
* [VASA-1: Lifelike Audio-Driven Talking Faces Generated in Real Time][VASA-1] [[Review][VASA-1_review]]
* ...

----

[VASA-1]: https://www.microsoft.com/en-us/research/project/vasa-1/
[VASA-1_review]: vasa1
