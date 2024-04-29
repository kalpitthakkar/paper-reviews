---
title: Talk3D Review
layout: page
parent: Talking Face Generation
nav_order: 2
---

# Summary

[Talk3D] aims at rendering talking face video from novel-views that are 3D consistent.
They provide conditioning in the NeRF space of the identity to generate video that
faithfully follows the audio signal and has 3D consistent face geometry when rendering
novel views not present in the monocular video for that identity.

This falls under our category of papers that use 3D primitives to have consistent
geometry when head pose is out of distribution from our training set. It's an add-on
to our basic requirements for a talking head generation system, albeit an important
and widely desired one.

Their [demo video] is pretty bad.
Even though it's a promising add-on to consider, their approach doesn't seem
to produce good results.

----

[Talk3D]: https://ku-cvlab.github.io/Talk3D/
[demo video]: https://www.youtube.com/watch?v=OkQtwWN0q00