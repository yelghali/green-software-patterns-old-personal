# Reduce carbon emissions of recurrent Tasks/Jobs, by scheduling them when Electricity Carbon Intensity is low
## Version
1.0

## Submitted By
Yassine El Ghali (@yelghali)

## Published Date
TBD

## Intent
Schedule recurrent workloads based on location-based marginal carbon emissions (aka Electricity Carbon Intensity), to reduce  their carbon emissions

## Tags
Cloud, Networking, Cloud Engineer, Small

## Problem
the carbon emissions of a software system depends on the power consumed by that sotware, but also on the Carbon intensity of the Electricity it is powered on. For this reason, running energy-efficient software on Carbon intensive Electtricity grid, might be inefficient to reduce its global carbon emissions. 

## Solution
Enable Carbon Aware time scheduling, for recurrent Jobs suchs as Crons, ML Training Jobs, Batchs, etc.

## SCI Impact
`SCI = (E * I) + M per R`

Regarding the SCI equation. Reducing the distance will impact:

- `I`: The goal is to reduce SCI by reducing (I), and in practice, schedule recurrent Jobs when I is low.


## Assumptions
the recurrent Job to be time shifted, has a flexible time window for scheduling, which allows variation on time to reduce (I). 

## Pros & Cons
- **PRO**: Applications / workloads can benefit from time shifting at the Platform Operating level, without requiring change to their code.
- **CON**: scheduling constraints for batchs or Crons, with several dependencies. 
