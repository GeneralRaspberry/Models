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

𝑠
𝑡
+
1
(
𝑖
)
=
𝐹
(
𝑠
𝑡
(
𝑖
)
,
𝑁
𝑡
(
𝑖
)
)
s
t+1
	​

(i)=F(s
t
	​

(i),N
t
	​

(i))

where:

𝑠
𝑡
(
𝑖
)
s
t
	​

(i) is the reinforcement state of cell 
𝑖
i at time 
𝑡
t,

𝑁
𝑡
(
𝑖
)
N
t
	​

(i) is the number of active neighbours,

𝐹
F is a nonlinear local update rule incorporating activation, reinforcement, and decay.

The introduction of reinforcement (a bounded increasing state variable) creates hysteresis in the system — meaning future states depend not only on current neighbourhood configuration, but also on accumulated past interactions. This transforms the automaton from a purely dissipative system into one capable of storing structured information over time.

In dynamical terms, stable patterns correspond to attractor regions in state space sustained by repeated local reinforcement under continuous perturbation.

