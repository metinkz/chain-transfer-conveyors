# Chain Transfer Conveyor System

A PLC-based chain transfer conveyor automation project developed in **Siemens TIA Portal** for exercising purposes.
The system enables object transfer between **differently positioned conveyor sections** using a chain transfer mechanism.
Sequential control logic and HMI-based animation are used to visualize and ensure safe operation.

## System Overview
- The system enters a **ready state** when the *Start* button is pressed.
- Conveyors are monitored using presence sensors to detect object occupancy.
- A chain transfer mechanism is used to transfer objects between differently positioned conveyor sections.
- System operation is visualized using HMI animations.

## Operating Sequence
When an object is detected on a conveyor and transfer conditions are satisfied, the following sequence is executed:

1. The **current conveyor stops**.
2. The **chain transfer mechanism moves to the transfer position**.
3. The **chain motor starts** and transports the object.
4. When the object reaches the next conveyor:
   - The **chain motor stops**.
   - The **chain mechanism returns** to its original position.

## Conveyor Handover Logic
- If the conveyor after the chain transfer is **not the last conveyor**, it starts running provided the next conveyor is not occupied.
- If the conveyor after the chain transfer **is the last conveyor**, it remains stopped until receiving the object.

## HMI Visualization
- Conveyor motion is represented using animated graphical elements.
- Chain transfer movement is animated to reflect the actual sequence.
- Animations are driven by sensor signals.

## Safety and Interlocking
- Conveyor and chain operations are interlocked using sensor-based conditions.
- If any conveyor involved in the transfer is occupied, the system does not start, even if the *Start* button is pressed.
- This logic prevents collisions, object accumulation, and unsafe operation.

## Tools & Technologies
- Siemens TIA Portal
- Siemens WinCC Advanced
- PLCSIM

## What I Learned
- Designing sequential control logic for chain transfer systems
- Coordinating conveyor and chain mechanisms for transfers
- Implementing HMI animations linked to sensor signals

## Possible Improvements
- The current HMI focuses on functional animation rather than visual design.
- The user interface can be improved with a more modern layout, clearer visual, and enhanced usability with alarms to keep track of any possible errors or warnings.

