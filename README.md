# Railway_Track_Damage_Detection_Robot

### Introduction
   A 4 wheeler robot that can detect damages on the railway tracks like dents, cracks using Ultrasonic sensors, 
captures images of the surroundings using pi camera and finally sends the images captured and the locations 
(coordinates) of the points where there are damages on the tracks to a database and the same data can be viewed
in a webapp which has log in features. We can log in into the respective railway station account and see the 
railway track damage data collected by their robot.

### Methodology
  The 4 wheeler robot has an Arduino Uno broad, a Raspberry pi, servo motor, pi camera and ultra sonic
sensors on it. The sensors face towards the ground i.e the railway tracks. When the robot starts, the 
ultrasonic sensors get activated, they are basically used to calculate the distance between the railway
track and the sensor, whenever there is a dent or any damage on the track, the distance between the
sensors and the track changes, when this change crosses a threshold value, then the robot decides that
there is a damage at that particular location.

  When a damage is detected, immediately the Arduino triggers the Rpi, then the Rpi ask for the 
coordinates of the location to the location API, also it activates the servo motor and pi camera to 
capture images of the surroundings. The Rpi sends the received coordinates and the images to the server
and the server uploads it to the database. This data can be viewed in the webapp with the log in feature.
