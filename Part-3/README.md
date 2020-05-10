# Micromouse Maze
## Motors
The original solution makes use of DC motors. I think stepper motors would be a better option.
### Pros
* Precise movement control
* Mounting is easier
### Cons
* Not very powerful as compared to DC motors but for the current application, it works well.
* Complex control requirements, but it can be overcome by a stepper motor controller.
## Sensors
* The Ultrasonic Sensor used in the front in the original solution can be replaced by an **IR Triangulation sensor** or an **IR ToF sensor**.
* Ultrasonic distance sensors offer comparatively **poor resolution** and **range** compared to other technologies.
* Ultrasonic distance sensors are susceptible to interference by **acoustic noise** and crosstalk from other sensors with the same frequencies.
* IR sensors are **cheaper** compared to Ultrasonic distance sensors.
* IR triangulation has a **small form factor** and a lightweight construction.
* However, IR distance sensors are generally short-range solutions.
