# Gas Compressor PLC–HMI Automation

## Problem
A gas compressor package needed repeatable, safe startup and shutdown with less manual intervention: no starts with active trips, controlled cranking and fueling, deterministic ESD, and clear alarms.

## Solution
- Permissive-based start (lead selection, no-flow switch, fuel scrubber, no active trips)
- Start gas → timed fuel admission → RPM-based crank cutoff (starter protection)
- Retry logic with attempt counter and cooldown; Start Fail alarm when attempts are exhausted
- Manual stop with cooldown, trip recovery timer before forced shutdown
- Immediate ESD overriding all logic; blowdown valve (BDV) logic on pressure conditions
- Latched alarms cleared only after the condition is safe and the operator resets
- HMI screens: status, alarms, setpoints, maintenance, trends

## Stack
Fatek FBs-60MAR with FBs 4AD / 6AD / 16TC modules · Weintek HMI (CMT2128x, 10") · WinProLadder · EasyBuilder Pro · Modbus RTU over RS-485 · 24 VDC
