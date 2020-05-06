# Hexapod
## Overall Structure
From an electronics point of view, there will be a hierarchy of controllers which will work in unison.
* 1 central controller
* 3 leg controllers
* 18 joint controllers

Each leg controller will control 2 legs and hence indirectly control 6 joints. These 3 leg controllers are inturn controlled by the main controller.

The joint controllers communicate with the leg controllers in an asynchronous manner and communication is initiated by the joint controllers. Same is the manner of communication between the leg controllers and the main controller.

## Sensors for present state detection
The sensors on this bot can be classified into internal sensors and external sensors, internal sensors for detection of the orientation and state of the bot, external sensors for evaluating the environment.
### Internal Sensors
* Rotary encoder for the angular position of the joints. As there are 18 joints, we will need 18 encoders.
* Inclinometers to detect the orientation of the bot with respect to the horizontal level. We will need two of them, one to detect front-back inclination, and the other to detect left-right inclination.
### External Sensors
* For each of the 6 legs, there can be contact sensors at the end of each of them to avoid emergency situations.
* Several Ultrasonic Distance Sensors attached around the body for obstacle detection purposes.
## Data Flow
* The data from the contact sensors at the leg end are sent to the corresponding leg controller. The feedback from the contact sensors ends at the level of the leg controller.
* Each joint controller uses angular values sent from the leg/main controllers and then provides a feedback loop using the digital encoders.
* The main controller gets data directly from the inclinometers and then accordingly directs the leg controllers in the case that recovery behaviour is required.
* The Ultrasonic Distance sensors send data directly to the main controller. The main controller directs the leg controllers accordingly based on the external environment.
