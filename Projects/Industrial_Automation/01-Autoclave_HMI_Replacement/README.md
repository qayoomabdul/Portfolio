# Autoclave HMI Replacement (Chinese → English)

## Problem
An industrial autoclave ran a Chinese-language MCGS HMI (TPC1162Hi) on a Siemens S7-200 CPU 226CN. Operators needed an English interface, but the original PLC program could not be modified.

## Solution
Built a new English HMI that talks to the existing PLC program unchanged, by reverse-engineering how the original HMI used the PLC registers.

- Traced 225+ unique registers across 74 networks of the ladder program
- Rebuilt a 12-segment temperature recipe and a 9-segment pressure recipe system
- Added trend graphs, alarms, and manual/auto control screens
- Set up MCGS ↔ S7-200 communication over RS-485/PPI

## Stack
Siemens S7-200 CPU 226CN · MCGS TPC1162Hi · STEP 7-MicroWIN · McgsPro scripting

## Result
HMI conversion completed without touching the original PLC program.
