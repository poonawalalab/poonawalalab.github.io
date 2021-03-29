@def class = "journal"
@def authors = "Jiang, J.; McCoy, A.; Lee, E.; Tan, L.;"
@def title = "Development of a Motion Controlled Robotic Arm"
@def venue = "IEEE"
@def year = "2015"
@def hasmath = true
@def review = true
@def tags = ["control", "robotic arm", "motion sensing", "accelerometer", "arduino uno"]
@def reviewers = ["David Yackzan"]

\toc
### Broad area/overview
This paper focuses on an inertial strategy using an Arduino Uno to control a robotic arm. A person attaches the sensor pack to their arm by using velcrow strops and wears a glove so that their motion can be measured by the system and mimicked by the robotic arm.

### Specific Problem
The authors outline the main goals of keeping the robotic arm light so that it will not have to lift a lot of its own weight (and thus will be relatively stronger and more maneuverable) and keeping the code efficient so that the response time of the robotic arm is quick.

### Solution Ideas
  * Sensors:
    - The inertial sensor set consists of 2 accelerometers attached to the user's arm, one for the forearm to measure $X$ and $Z$ directions of movement and one for the bicep to measure the $Y$ direction of movement.
    - The authors also incorporate a Triple-Axis Compass to assist the IMUs in provding accurate directional data to the Arduino.
    - A flex sensor is attached to a glove so that when the user flexes their hand, the resistance in the sensor will change and the claw on the robotic arm can be controlled to mimick the motion.
  * Actuators: The robotic arm is controlled through 6 servomotors
    - 2 servos for the wheels
    - 2 servos to actuate the shoulder of the robotic arm
    - 1 servo to actuate the elbow
    - 1 servo to actuate the hand
  * The robotic arm is controlled through 4 buttons and the inertial data coming from the imus and compass attached to the user's arm. The buttons are used to control the wheels on the robot base for forward, backwards, and rotational motion concerning the wheels.

### Comments
* This paper did not mention any details on control strategies used for translation of the sensor data into robot motion so while it may have functioned as intended, it is unlikely that the motion of the robotic arm was exceedingly well-responsive to the sensor input.

### Recent Papers
* This 2020 paper outlines more recent research pertaining to a similar project: *Controlling a robotic arm for functional tasks using a wireless head-joystick: A case study of a child with congenital absence of upper and lower limbs*
  - https://saa-primo.hosted.exlibrisgroup.com/primo-explore/fulldisplay?docid=TN_cdi_plos_journals_2430651123&context=PC&vid=UKY&lang=en_US&search_scope=default_scope&adaptor=primo_central_multiple_fe&tab=default_tab&query=any,contains,inertial%20control%20robotic%20arm&mode=Basic
