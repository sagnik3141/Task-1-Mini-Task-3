# Micromouse Maze
## Motors
The original solution makes use of DC motors. I think stepper motors would be a better option.
### Pros
* Precise movement control
* Mounting is easier
### Cons
* Not very powerful as compared to DC motors but for the current application, it works well.
* Complex control requirements, but it can be overcome by a stepper motor controller.

**28BYJ-48 Stepper Motor** and **ULN2003 Stepper Motor Driver** are good options.
## Sensors
* The Ultrasonic Sensor used in the front in the original solution can be replaced by an **IR Triangulation sensor** or an **IR ToF sensor**.
* Ultrasonic distance sensors offer comparatively **poor resolution** and **range** compared to other technologies.
* Ultrasonic distance sensors are susceptible to interference by **acoustic noise** and crosstalk from other sensors with the same frequencies.
* IR sensors are **cheaper** compared to Ultrasonic distance sensors.
* IR triangulation has a **small form factor** and a lightweight construction.
* However, IR distance sensors are generally short-range solutions.
* **RKI-3141 IR sensor** is a great option.
* The **GY-53 VL53L0X Laser ToF Sensor** should be retained from the original solution.
* **RKI-5103** which is a rotary encoder will also be required to determine the distance travelled.
## Microcontroller
In my opinion, the **ESP32** board is well suited for the micromouse because it is powerful, lightweight and has sufficient memory.
## Power Supply
* A 5V power bank should do the job.
* **28BYJ-48 Stepper Motor** and **ULN2003 Stepper Motor Driver** should be connected to the 5V supply.
* **RKI-3141 IR sensor** should be connected to the 3.3V supply.
* **GY-53 VL53L0X Laser ToF Sensor** can be connected to either.
## Algorithm
* After doing a little research, I found that Micromouse Robots generally use one out of the three algorithms: **Wall Following**, **Depth First Search** and **Flood Fill**.
* Out of these, Wall Following is not very useful because most mazes are designed such that this algorithm will fail.
* Depth First Search goes through the full maze and it takes a lot of time.
* This leaves us with **Flood Fill** Algorithm.
