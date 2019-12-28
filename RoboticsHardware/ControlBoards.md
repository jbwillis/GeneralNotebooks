# Robotics Control Boards
**27-Dec-2019**

I have been interested in getting a general purpose robotics platform for doing experiments and class projects. This would include some sort of ground robot, as well as electronics that I could use to control the ground vehicle as well as other robotics projects. The options that I have found for robot platforms and electronics are listed below, along with features I find important.

## Mechanical Platforms
This section includes the mechanical structure of the robot as well as the motors.
### Desired Features
* Shoebox-scale dimensions
  * Large enough to easily hold a camera and some extra electronics. 
* Extendable surface - easy to securely mount additional sensors, hardware, etc
* Encoder feedback on drive motors
* Position feedback on steering motors
* Rugged enough for outdoor use (such as in a parking lot)

### Options
#### [ARobot](https://www.arrickrobotics.com/arobot/)
[**Documentation**](https://www.dropbox.com/home/Reference/other/ARobot)

My parents purchased this for me when I was in 9th grade so I could use it for a class project (to build a line following robot). I had problems with my sensor (which looking at it now is an absolute ratsnest, so I'm not suprized), so I have never really done anything with the robot.

This is a three-wheeled design. There is one drive wheel and two steering wheels. It is approximately 10"x10" and has lots of options for mounting. It steers by turning two wheels with a servo - this would give decent position feedback. It also includes a 20 tooth encoder on the drive wheel. I would want to replace it with a better encoder.

Drive motor is 12V geared, 74 RPM full load, 1.6A full load. H-Bridge driver is 1A full load. Typical motor current draw is .2A.

**Pros:**
* I already own it!
* Meets most of my feature requirements

**Cons:**
* Encoder isn't great (only 20 teeth)
* Mostly designed for indoor environments
* Requires a total rewire (shouldn't be too much work)

#### Lego Mindstorms Kit
This is another kit I already own. The hardware is all in great condition, but unfortunately the mindstorms programming environment (which has always been limited) is not supported on modern windows computers. 


## Control Electronics
This section includes all of the core electronics necessary to get the robot running. This includes things such as motor drivers and the controller sending commands to the motor drivers, but not necessarily the computers for high-level tasks like robotic vision. 

### Desired Features
* Separation of control and computation. One of the problems with my current robotics platforms is they were designed with the assumption that all computation would take place on an 8 bit microcontroller (such as the BASIC Stamp). This no longer matches my needs - I want a mobile platform that can receive commands from a computer performing computationally intensive tasks like machine vision. If the control electronics had been designed with a sufficient degree of separation from the computation electronics, it would be easy to upgrade computation and keep the control system the same. 

### Options
#### [BeagleBone Blue]()
This is a robotics-specific model of the BeagleBone Black embedded linux computer. It adds motor controllers, 2-cell LiPo battery management, WiFi, an MPU9250 IMU, and more! The [EduMIP](https://beagleboard.org/p/edumip/edumip-13a29c) project is a fun looking self-balancing robot kit that uses the BBBlue.

**Pros:**
* There is lots of support out there for the BBBlack, which means the linux side of using the BBBlue would be easier.
* People have run ROS on the BBBlue - [the EduMIP project shows how to set this up](https://dscl.lcsr.jhu.edu/home/courses/edumip_ros/#Notes_on_Running_EduMIPwith_ROS)
* Built-in wifi
* With some small modifications, it can [drive Lego mindstorms motors](https://lechnology.com/2017/03/using-lego-mindstorms-motors-with-beaglebone-blue/), and can be [mounted to Lego technic pieces](https://lechnology.com/2017/03/mounting-a-beaglebone-blue-to-your-lego-mindstorms-robot/). 
* Probably the quickest way to get a system up and running.
* Supported by ArduPilot

**Cons:**
* Insufficient separation of control and computation - the BBBlue was first produced in 2017, which means it is likely already near its end of life. I could instead (for more money) buy a beaglebone black and the beaglebone black robotics cape.
* Expensive ($80)
* JST connectors used for everything
  * There is a jumper bundle available [here](https://www.renaissancerobotics.com/JST_Jumper_Bundle.html)
    * It includes: 4 2-pin 1.5mm JST-ZH female connectors (motors), 8 4-pin 1.0mm JST-SH female connectors (encoders, I2C, CAN, PWR), and 4 6-pin JST-SH female connectors (SPI, GPS, GPIO, ADC)

#### 
