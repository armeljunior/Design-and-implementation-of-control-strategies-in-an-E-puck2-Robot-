# Design-and-implementation-of-control-strategies-in-an-E-puck2-Robot-
Robots are put in strenuous circumstances which require hardware as well as algorithms and expertise to adapt and move in these conditions. The robots are placed in controlled environments encompassing a greater challenge to manoeuvre around obstacles in the most optimal way possible, Collison avoidance. The E-pucks successfully managed to maneuver around a closed environment with no obstacles in the way, with a low chance of collision with dynamic objects placed in the environment. Moreover, tasked with following an object with some avail as this was possible, although when this was not directly in front of the e-puck this was not possible. 
Keywords-  Fuzzy Logic controller, collision avoidance, line 
following, mobile robots, data fusion, dynamic obstacles.
Keywords: collision avoidance, object following, dynamic obstacles, environment


asynchronous receiver-transmitter)
The dsPIC within the Microcontroller of the E-puck has two Uarts. The LMX9820A can be accessed transparently using the bluetooth rfcomm channel to ensure data is successfully sent to and from communication of the e–puck robot Bluetooth Communication is setup. This is set up by enabling and testing hello world to and from the robotic device to the PC. The Address of the Robot’s MAC address is taken and programmed to be link with UNIX to be able to read real time data with minimal delay.
Sending and receiving sensor data
The E-puck robot consists of 8 IR proximity sensors. Linking the real time bluetooth communication with the readings in the E-puck we are now able to send and receive each of the individual sensor data corresponding to 8 counter directions shown in Figure 1. The range of the IR sensors show that an object within 15cm gave a reading of ≈ 150. This data allows for a threshold to be created on when to manoeuvre the robot either in avoidance or following.
 
Figure 1 Directions of sensors
Setting up Motors
The movement system of the e-pucks robot consists of 2 wheels connected with 2 stepper motors with a 50:1 reduction gear. There are two motors on the E-puck Robot. Allowing the robot to manoeuvre in all directions possible as well as small spaces. Tests were taken to understand the difference in turning left and right, something explored was to either have one wheel stop, and the opposite wheel continues to rotate when turning or to simply rotate both wheels.  

Obstacle Avoidance 
Task 1 involved designing implementing and testing a control strategy for an E-puck robot. The criterion being considered is the ability to explore a bounded environment with dynamic obstacles as well as avoid the environment boundary or obstacles.

The initial strategy behind using the obstacle avoidance algorithm created started with deciding to use all the sensor values combined. However, this led to complications in the algorithm created which resulted in the robot to jitter due to each of the sensor values spiking unexpectedly. As a result, an algorithm was implemented which involved 4 sensors instead of all 8. This worked by as shown in Figure 2 to go forward at all instances unless the front and side sensors threshold was exceeded. If these were exceeded an orientation change was made by adjusting the motors.

 
Figure 2 Obstacle Avoidance Pseudocode

Object Following

The task at hand involves designing, implementing, and testing a control strategy with the ability to chase an object in an open environment, building upon this would involve no collision with the object. The initial design behind this algorithm was to have each of the individual sensor values with a set threshold opposite to that of object avoidance. However, in a practical environment, the issue was that too many sensor readings would result in a large chain of commands, therefore a new strategy was to be implemented. This new algorithm instead uses fewer sensors however, to ensure all degrees around the robot are covered the robot is to be continuously rotating. Therefore, if anything is within the bounds of the robot at the threshold value there will be a movement towards this.

 
Figure 3 Object following Pseudocode

Results
Following Task 1 criterion, the Algorithm produced resulted in the robot successfully exploring the environment it was confined in. However, the robot would collide with the dynamic object sporadically with no consistency.
Task 2 resulted in the e-puck successfully being able to chase an object at a stay at 3 cm in an open environment however, this was only successful when the object was directly in front of the robot.
Conclusion
In conclusion, there are many things which could be improved. Firstly, within task 1 there is a major factor with more time that could be implemented to improve our control algorithm. Had there been more time if all 8 sensors were successfully considered to prevent interference between sensor data this would have led to a smoother running of the robot due to less or no collisions with walls. To improve the results of task 2 this could be achieved using all the sensors which would allow the robot to steer itself and follow if there was an object behind the robot, therefore, allowing the robot to see all directions and would no longer have to rotate in a circle continuously.
