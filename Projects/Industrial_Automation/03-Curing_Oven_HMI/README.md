# Curing Oven HMI

## Overview
MCGS HMI and Siemens S7-200 SMART control for a curing oven with a recipe-driven temperature ramp/hold sequence.

## Hardware
- 3 temperature points (top / middle / bottom)
- 2 blowers, 1 damper valve
- 12 heaters in 4 groups of 3

## HMI
- Screens: Manual, Auto (trend + segment table), Monitor, Real-time curve, Recipe table, Alarms
- Recipe-control script running in the cyclic background strategy
- In progress: date-wise saved curves, viewable from a run-history table

## Stack
Siemens S7-200 SMART · McgsPro
