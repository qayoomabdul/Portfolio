# Thread Length Measurement

## Overview
Measures thread length on a winding drum using a Delta PLC and a rotary encoder.

## Implementation
- Delta DVP14SS2 PLC with Omron E6B2-CWZ6C encoder (360 PPR, NPN, A/B/Z)
- High-speed counter (C251, 2-phase) for quadrature counting
- Encoder coupled to the contact-roller shaft with a flexible jaw coupling
- Calibrated empirically from repeated 609.6 mm test runs (~0.061 mm per pulse)
- Fixed missed counts by tying the grounds of the separate power supplies together

## Stack
Delta DVP14SS2 · Omron E6B2-CWZ6C

## Media
- [ ] Setup photo
- [ ] Wiring diagram
