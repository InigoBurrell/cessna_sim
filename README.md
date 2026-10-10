Cessna Sim

===Requirements===
- MATLAB 2025a
- Simulink
- Aerospace Blockset

===User Guide===
- Before running the simulation, load the data from "cessnadatcom.mat" into the MATLAB workspace
- When this .mat file has been loaded, the "DATCOM Forces & Moments" block inside the "Calculate Forces & Moments" subsystem will need to be regenerated
- Once this block has been regenerated, the bottom two inputs (dalpha/dt and w) will need to be re-connected
- Scopes are contained within the "Scopes" subsystem

===Purpose===
- To learn how to use Digital DATCOM to generate flight dynamics and stability data for an aircraft configuration
- To practice building a 6-DOF flight dynamics model
- To compare the model against existing flight-test data
- To practice the implementation of control strategies beyond PID, such as full state feedback

===Known Issues/Limitations===
- Thrust is currently modelled as a simple constant force; no propeller gyroscopic or slipstream effects are modelled
- The effect of rudder deflection is not currently modelled
- The Cg location used to calculate the data in Digital DATCOM is likely too far forward, as the aircraft struggles to fly level
- Cg location, mass and moments of inertia do not change as the aircraft burns fuel

===Next Steps===
- Re-compute Digital DATCOM data with different Cg locations
- Model propeller gyroscopic and slipstream effects
- Model the effect of rudder deflection
- Compare against flight test data
- Implement control/mode-shaping strategies
