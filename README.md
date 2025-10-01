# chain-transfer-conveyors
Automation of conveyors with chain attached, allows objects to be transferred across differently positioned conveyors. Made in TIA Portal.

Start button sets the system in ready state, if sensors detect any objects, current conveyor and next conveyor start to work and transfer the object.
If sensor detects the object in chain conveyor, sequence is stated as below:
- Current conveyor stops,
- Height of the chain goes up,
- Motor starts to run for transportation of the object on chain,
When object reaches to next conveyor,
- Motor stops, therefore, chain stops working.
- Height of the chain goes back to it's original state.
- If conveyor at the end of the chain is the last conveyor;
  - Last conveyor does not work,
  - Otherwise, it works normally as long as the next conveyor is not occupied.
 
If conveyors are occupied, even if the start button is triggered, system does not run to prevent collision or any accident.
