---
title: "Torus Flow with Particle Feedback"
permalink: /torus-feedback/
---


This post explores a minimal system where particles locally rotate a flow field.

<div style="margin: 2rem 0; width: 100%;">
  <iframe
   src="https://editor.p5js.org/GeneralRaspberry/full/2jODsztoC"
    width="100%"
    height="480"
    style="border: 1px solid #ddd; border-radius: 8px;"
    loading="lazy"
  ></iframe>
</div>

<p>
<a href="/Models/models/torus-flow/" target="_blank">
Open model in new tab →
</a>
</p>

---

### Model description

A uniform force field is defined on a two-dimensional domain with toroidal topology.

Particles are introduced. Each particle applies a local rotational perturbation to the field with strength 
𝛼
α, where
\[
\alpha = \text{rad} \cdot \text{particle}^{-1} \cdot \text{frame}^{-1}
\]
At each frame, the evolution of the field is determined by the sum of particle contributions.

The resulting dynamics are chaotic.

At low particle speeds, motion is dominated by local two-dimensional structures. As particle speed increases, these local structures weaken and coherent global behaviour emerges in the form of three-dimensional super-structures.

By extension, if the system were embedded on a higher-dimensional torus, further increases in speed would be expected to produce higher-dimensional coherent structures.

One particle is marked blue to demonstrate the behaviours.
