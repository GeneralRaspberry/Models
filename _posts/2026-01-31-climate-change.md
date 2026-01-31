---
title: "Climate Change from first principles"
permalink: /climate_change/
layout: default
---


This post explores a climate change from first principles.

<div style="margin: 2rem 0; width: 100%;">
  <iframe
   src="https://editor.p5js.org/GeneralRaspberry/full/VR1475f0O"
    width="100%"
    height="1000"
    style="border: 1px solid #ddd; border-radius: 8px;"
    loading="lazy"
  ></iframe>
</div>

<p>
<a href="/Models/models/_climate_change/" target="_blank">
Open model in new tab →
</a>
</p>

---

### Model description


This post presents a minimal, first-principles toy model exploring how non-linear climate dynamics emerge when a system is formulated in terms of accumulation rather than instantaneous flux.

An initial flux-based formulation produced largely linear behaviour and failed to capture qualitative features observed in real climate systems. Reformulating the model to include memory — by accumulating carbon over time — fundamentally altered its dynamics.

---

## Model structure

Photosynthesis is modelled as a temperature-dependent process with an optimal temperature $$T_{\mathrm{opt}}$$, represented by a Gaussian response curve. The parameter $$\sigma$$ controls the breadth of this response and reflects how tightly plant productivity is tuned to its optimum.

Respiration is modelled relative to temperature using a $$Q_{10}$$-type relationship. In this formulation, respiration acts as a **metabolic burn rate**: higher respiration increases carbon release while simultaneously reducing the system’s capacity to sustain photosynthesis.

Net ecosystem production (NEP) is defined as the balance between respiration and photosynthesis. Rather than treating NEP as an instantaneous flux, it is accumulated over time to represent atmospheric carbon stock.

Temperature responds logarithmically to deviations from a baseline carbon level, introducing a non-linear climate forcing.

---

## Emergent behaviour and fragility

The model exhibits strongly non-linear dynamics.

Wider photosynthetic tolerance ranges $$\sigma$$ substantially dampen temperature excursions, while lower optimal photosynthesis temperatures $$( T_{\mathrm{opt}} ) \$$ reduce long-term warming. These stabilising effects arise without explicit control mechanisms and emerge purely from accumulation and feedback.

Increasing temperature sensitivity does not significantly alter the eventual temperature range. Instead, it increases the rate at which the system cycles between temperature states, suggesting that external processes which amplify climate sensitivity may primarily affect **system volatility rather than equilibrium temperature**.

The system is fragile. Small changes in respiration rate or temperature sensitivity can shift the dynamics from stable oscillation to runaway behaviour. Because respiration simultaneously accelerates carbon release and suppresses photosynthetic capacity, feedbacks compound rapidly once critical thresholds are crossed.

---

## Interpretation

Although highly simplified, the model demonstrates how non-linear behaviour can arise from minimal assumptions when memory and feedback are introduced.

The balance between photosynthetic breadth, metabolic burn rate, and temperature sensitivity governs whether the system stabilises, oscillates, or destabilises. This toy model is not predictive, but it highlights how coupled biological–climate systems can exhibit fragility and regime shifts even under simple rules.
