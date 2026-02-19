---
title: "Order From Chaos: Cellular Automata"
permalink: /Order_from_chaos/
layout: default
---


This post explores order from chaos with a simple cellular automata rule.

<div style="margin: 2rem 0; width: 100%;">
  <iframe src="https://editor.p5js.org/GeneralRaspberry/full/v55UVH6r6"></iframe>
</div>

<p>
<a href="/Models/models/Order_from_chaos/" target="_blank">
Open model in new tab →
</a>
</p>

---

### Model Summary & Findings

In this project, I developed a memory-based cellular automata model in p5.js to explore how local interaction rules can generate persistent order from microfluctuations.

Each cell in the grid follows a simple recursive rule:

A cell activates when exactly one neighbour is active.

Activity reinforces over time when stable local conditions persist.

Overcrowding or isolation causes decay.

User clicks introduce small, local perturbations (microfluctuations).

Two parameters allow exploration of different dynamical regimes:

Decay (toggleable): When enabled, isolated pixels gradually lose reinforcement and return to zero. This removes unsupported structure and increases selective pressure, but it is not strictly necessary for pattern formation — order can still emerge through reinforcement and overload dynamics alone.

Maximum state 𝐾 (slider-controlled): This sets the upper bound on reinforcement. Larger values of 
𝐾 increase the tolerance and persistence of stabilised structures, allowing deeper memory accumulation before decay or destabilisation occurs.

Frame rate (slider-controlled): This sets the rate at which the frames are updated per second, allowing the user to fine-tune their influence on the system and see the dynamics unfold.

Initially, the system appears noisy and unstable. However, after only a few perturbations, structured regions begin to stabilise. The key mechanism behind this behaviour is rapid entropy fluctuation within local pockets of the grid. Because activity propagates through narrow channels (exactly one-neighbour conditions), certain cells repeatedly come into contact with partially stabilised neighbours. This repeated interaction reinforces specific pathways.

As a result:

Transient fluctuations self-filter.

Some cells accumulate memory (reinforcement levels).

Stable patterns emerge without central control.

Order is not imposed — it is selected.

Equilibrium in the system is not static. Instead, it is dynamically maintained. Entropy continues to fluctuate locally, but at a speed that sustains reinforcement in particular regions. These semi-stable cells act as anchors for emergent structures, leading to coherent pattern formation across the grid.

---

### Mathematical Framing

Formally, the model can be described as a discrete-time dynamical system:

$$
s_{t+1}(i) = F\big(s_t(i), N_t(i)\big)
$$

where:

- $s_t(i)$ is the reinforcement state of cell $i$ at time $t$,
- $N_t(i)$ is the number of active neighbours,
- $F$ is a nonlinear local update rule incorporating activation, reinforcement, and decay.


The introduction of reinforcement (a bounded increasing state variable) creates hysteresis in the system — meaning future states depend not only on current neighbourhood configuration, but also on accumulated past interactions. This transforms the automaton from a purely dissipative system into one capable of storing structured information over time.

In dynamical terms, stable patterns correspond to attractor regions in state space sustained by repeated local reinforcement under continuous perturbation.

