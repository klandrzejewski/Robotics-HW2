# Robotics-Project

This repository contains the indoor simulation for part 1 of the project for CS 560 - Autonomous Robotics by Kaleigh Andrzejewski.

The indoor simulation is a model of the first floor of Bruno Library at the University of Alabama. 
The file can be found under the Resources folder as bruno.wbt and under the webots_ros2_project1_python\worlds\bruno.wbt.

To launch the simulation, follow the steps provided by Dr. Monica Anderson from HW 1 that is included in the README.md under webots_ros2_project1_python.

### Changing Lighting
To change the lighting, open up the bruno.wbt file under the worlds folder in Webots. On the left side of the screen, there will be multiple Prontos to represent the furniture and building features of the library. The Prontos labeled "CeilingLight" and the two labeled "FloorLight" will allow you to manipulate the lighting. 

The easiest way to find the light you desire to switch, simply left click to select the light fixture and its respective Pronto will be highlighted on the left. In the dropdown for the light, there is a attribute labeled "pointLightIntensity". The default for this is 5. Switch this value to 0 to turn off the light, or to 5 to turn it back on. You can manipulate this value to dim or brighten the light as needed, but ensure that the value remains positive (greater than or equal to zero). Note that Webots has a maximum for how many lights can be rendered, so if an issue is encountered where certain lights are not displaying as intended, try to turn off other lights. 

### Changing Doors
To allow for a door to be able to open, open up the bruno.wbt file under the worlds folder in Webots. On the left side of the screen, there will be multiple Prontos to represent the furniture and building features of the library. The Prontos labeled "Door" represent all of the doors.

As previously mentioned, the easiest way to find the desired door is to left click in the simulation. From there the following attributes must be changed:

1. canBeOpen (True = door can be opened, False = door cannot be opened)

Under doorHandle doorLever:
2. canTurn (True = door can be opened, False = door cannot be opened)
3. hasStaticParent (True = door cannot be opened, False = door can be opened)

It should be noted that Webots doors require the robot to interact with the door to open it.
