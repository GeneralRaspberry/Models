---
title: "Vector-borne Pathogens: A novel approach to calculating R0"
permalink: /Vector_Model/
layout: default
---

Vector-borne Pathogens: A novel approach to calculating R0

Dr Thomas Taylor
No Affiliation
10/07/2026

Abstract

The proliferation of novel vector-borne diseases is directly linked to climate change. Here, I develop a spatially stochastic epidemic simulation model with vector-borne transmission between plants. I increase the abundance of vectors (v) and the attractiveness of infected plants (A), and measure the numbers of successful epidemics (infected plants >= 5). I implement 250 simulations per combination of v and A, with a time step of 14 days using Gillespie's tau algorithm. The landscapes were generated using a poisson mátern process, with a randomisation factor. My results show that R0 can be directly calculated with this model, indicating that the force of infection is partially a product of the distance between plants, vector abundance, vector preference and the rate at which plants are removed. This research will lead to better surveillance modelling, with critical information related to surveillance monitoring.

Introduction

The onset and proliferation of novel vector-borne diseases in the plant world is increasing (Spence, 2020). Vector-borne pathogens and diseases such as Xylella, Pierce's Disease, and various other grapevine diseases are posing threats globally due to their rapid dissemination through multiple species per pathogen (Castro, 2021). Xylella for example is a severe disease that has a unique relationship with the vectors known as sharpshooter leafhopper (Cicadellidae) and spittlebug (Cercopidae). It threatens many crops globally.

It is well known that there are associations between vector abundance and the onset of a disease epidemic (Donnelly & Gilligan, 2021). Increases in vector abundance due to changes in global temperatures and subsequent climate change have led to new pathways of emergence for plant pathogens via their vectors (Tsai et al., 2022). Furthermore, the dynamics between pathogens and vectors are largely unexplored due to their myriad presentations and complex interactions (Cunniffe et al., 2015). 

This paper seeks to strike light on one particular model of vector abundance, and how it largely determines the onset or extinquishment of an epidemic according to the well established idea of a basic reproduction ratio (Wadkin et al., 2024). This is typically calculated in simulation models by the number of individuals a single plant will infect. However, computation can be expensive, and mechanistic determinations or approximations of this value are invaluable to epidemiological modellers, especially in the context of surveillance.



