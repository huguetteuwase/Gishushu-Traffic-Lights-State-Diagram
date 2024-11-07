# Gishushu-Traffic-Lights-State-Diagram
Traffic Light Specification for 8-Way Intersection
1. Overview: This specification describes the states, timing, and behavior of traffic lights for an 8-way intersection, accommodating vehicle traffic from North-South and East-West directions. Pedestrian crossing and emergency override modes are included for safety and efficiency.

2. States & Timing:

State Descriptions
NorthSouth_Green:

Vehicle Direction: North-South lanes proceed.
Signal: North-South Green, East-West Red.
Duration: 45 seconds.
NorthSouth_Yellow:

Transition: North-South traffic is alerted to stop.
Signal: North-South Yellow, East-West Red.
Duration: 5 seconds.
NorthSouth_Red (Transition Delay):

Transition: All directions hold red for a safety buffer.
Signal: All directions Red.
Duration: 2 seconds.
EastWest_Green:

Vehicle Direction: East-West lanes proceed.
Signal: North-South Red, East-West Green.
Duration: 45 seconds.
EastWest_Yellow:

Transition: East-West traffic is alerted to stop.
Signal: North-South Red, East-West Yellow.
Duration: 5 seconds.
EastWest_Red (Transition Delay):

Transition: All directions hold red for a safety buffer.
Signal: All directions Red.
Duration: 2 seconds.
Pedestrian Crossing Phase
Pedestrian_Crossing:
Traffic Signal: All directions Red.
Pedestrian Signal: Walk signals active.
Duration: 20 seconds (depending on intersection size and pedestrian volume).
Conditions: Activated after East-West cycle or by demand button press, allowing pedestrians to cross safely in all directions.
Emergency Mode
Emergency_Stop:
Condition: Triggered by an emergency signal (e.g., from a central control system).
Signal: All directions flashing Red.
Duration: Indeterminate; remains active until emergency signal clears.
Transition: Upon emergency signal clearance, the system resumes normal operation at the North-South Green phase.
3. Timing Configuration Summary

NorthSouth Green: 45 seconds
NorthSouth Yellow: 5 seconds
NorthSouth Red (Transition Delay): 2 seconds
EastWest Green: 45 seconds
EastWest Yellow: 5 seconds
EastWest Red (Transition Delay): 2 seconds
Pedestrian Crossing: 20 seconds (adjustable)
Emergency Stop: Indeterminate
4. Operational Rules:

Normal Cycle:

Sequence follows the order: NorthSouth Green → NorthSouth Yellow → NorthSouth Red (Delay) → EastWest Green → EastWest Yellow → EastWest Red (Delay) → Pedestrian Crossing (if needed) → NorthSouth Green.
Pedestrian Phase:

Pedestrian crossing is activated at the end of each complete cycle or upon a demand signal. During this phase, all vehicle signals are red.
Emergency Mode:

Upon emergency signal, all vehicle lights flash red, allowing for emergency vehicles to pass safely. The system resumes normal cycle after the emergency clearance signal.
5. Safety & Efficiency Considerations:

Transition Delays ensure safety by holding all lights red before changing to the opposite green phase, preventing intersection conflicts.
Pedestrian Crossing Integration accommodates pedestrians without interrupting the flow of traffic during peak times.
Emergency Mode allows for emergency priority without disrupting the system’s overall operation post-clearance.
![alt text](https://github.com/huguetteuwase/Gishushu-Traffic-Lights-State-Diagram/blob/main/tetahuguette%2025513.drawio.png)
