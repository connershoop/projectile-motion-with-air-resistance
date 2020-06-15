# projectile-motion-with-air-resistance

## What does this do?
  
This function calculates the `distance`,`time of flight`, and `maximum height` for the flight of a projectile, fired over flat ground, experiencing air resistance proportional to its velocity squared.

## Instructions for use
`npm i projectile-motion-with-air-resistance`

`projectile(initalVelocity,launchAngleInRadians, dragCoeffiecient, mass, crossSectionalArea, gravitationAlCoefficient, airDensity)`
```
import projectile from 'projectile-motion-with-air-resistance

console.log(

  projectile(
    initalVelocity=10, 
    launchAngleInRadians=0.5, 
    dragCoeffiecient=4, 
    mass=3, 
    crossSectionalArea=2, 
    gravitationAlCoefficient=9.82, 
    airDensity=1 )
    )

// Output: 
//  {
//    maximumHeight: 0.33662516367922946,
//    horizontalRange: 1.3804636233789596,
//    timeOfFlight: 0.5067819524975948
//  }
```
## Parameters
* **initalVelocity**: Initial velocity of the projectile in meters per second.
* **launchAngleInRadians**: Launch angle of the projectile in radians.
* **dragCoeffiecient**: Drag coefficient of the projectile. (spherical projectile)
* **mass**: Mass of the projectile in kilograms (kg).
* **crossSectionalArea**: Cross-sectional area of the spherical projectile in meters. (pi * radius^2)
* **gravitationAlCoefficient**: Acceleration due to gravity in meters per second squared (m/s^2). 
  * default: 9.81
* **airDensity**: Density of the air (fluid) which the projectile is traveling through in kilograms per meters cubed (kg/m^3)
  * default: 1.29

## About this repository
This repository is the source of the projectile-motion-with-air-resistance npm package,  It is a function that uses numerical integration and newtons method to calculate the distance, time of flight, and maximum height of a projectile experiencing air resistance proportional to velocity squared.  See https://en.wikipedia.org/wiki/Projectile_motion for more information on this interesting problem in physics. This code is heavily based on the example given there.

## Why does this matter?
The solution for this problem with air resistance proportional to the velocity of a projectile is solved analytically.  In other words, there is a known solution for every situtation.  However, air resistance does not usually act that way, and for, say, a baseball, the air resistance is more closely proportional to the velocity squared of the object. This problem is not solved analytically, and needs to be approximated with a variety of common numeric methods.  

## What does it accomplish
This package accomplishes that solution to the problem described above, in javascript, in case anyone ever wants to do these calculations in a web browser.

## What can be improved? 
The approximations surroudning numerical integration, and newton's method could be improved.  The air resistance proportional to the velocity (not velocity squared) could be factored in.  As well as the velocity cubed.  The density of air is assumed to be constant with height, as is the acceleration due to gravity, neither of which is true. The curve of the earth is not accounted for. This is only a spherical projectile, other shapes could be accounted for. The drag coefficient could also be accounted for 
