# Robotics-Project

This folder contains the indoor simulation for part 2 of the project for CS 560 - Autonomous Robotics by Kaleigh Andrzejewski.

The outdoor simulation is a model of a .5 square mile of Tuscaloosa at the University of Alabama. An image of this area can be found as tuscaloosaGoogleEarth.jpg and below.

![Google Earth of Area](relative%20tuscaloosaGoogleEarth.jpg?raw=true "Map")

The file can be found under the webots_ros2_project2_python\worlds\tuscaloosa.wbt.

To launch the simulation, follow the steps provided by Dr. Monica Anderson from HW 1 that is included in the README.md under webots_ros2_project2_python.

### Changing Lighting
To change the lighting and time of day, open up the tuscaloosa.wbt file under the worlds folder in Webots. On the left side of the screen, there will be multiple Prontos to represent the world, roads, buildings, and other outdoor features. The Pronto labeled "TexturedBackgroundLight" and the Prontos labeled "StreetLight" will allow you to manipulate the lighting. By changing the attribute "luminosity" in "TexturedBackgroundLight" to 0, the world will be in nighttime mode, and changing it back to 1 will become day.

The easiest way to find the street light you desire to switch, simply left click to select the light fixture and its respective Pronto will be highlighted on the left. In the dropdown for the light, there is a attribute labeled "on". The default for this is FALSE. Switch this value to TRUE to turn on the light, or to FALSE to turn it back off. You can modify the intensity of this light by the "intensity" attribute which has a default of 30. Note that this value must remain greater than or equal to 0. 

Note that Webots has a maximum for how many lights can be rendered, so if an issue is encountered where certain lights are not displaying as intended, try to turn off other lights. 

### Changing Traffic Controls
To change the traffic controls, left click to select the traffic light you wish to change or select it from the list of Protos on the left side of the simulation. There are two types of traffic lights in this world: GenericTrafficLight and CrossRoadsTrafficLight.

For "GenericTrafficLight", the following attributes will modify the controls:

1. startGreen (True = light starts as green when world loads, False = light starts as red when world loads)
2. greenTime (How many seconds light should be green, default is 60)
3. redTime (How many seconds light should be red, default is 15)

For "CrossRoadsTrafficLight", to modify the controls, you would select "edit" under the "controller" attribute. In the text editor in Webots, the controller will open for you to modify. If you wish to change the light times, change the value listed after "t" in the if statements. The if statements are properly commented so you will know what you are changing.
