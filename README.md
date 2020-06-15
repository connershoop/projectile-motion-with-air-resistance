# projectile-motion-with-air-resistance

## About this repository
This repository is the source of the projectile-motion-with-air-resistance npm package,  It is a function that uses numerical integration and newtons method to calculate the distance, time of flight, and maximum height of a projectile experiencing air resistance proportional to velocity squared.  See https://en.wikipedia.org/wiki/Projectile_motion for more information on this interesting problem in physics. 

## Why does this matter?
The solution for this problem with air resistance proportional to the velocity of a projectile is solved analytically.  In other words, there is a known solution for every situtation.  However, air resistance does not usually act that way, and for, say, a baseball, the air resistance is more closely proportional to the velocity squared of the object. This problem is not solved analytically, and needs to be approximated with a variety of common numeric methods.  

## What does it accomplish
This package accomplishes that solution to the problem described above, in javascript, in case anyone ever wants to do these calculations in a web browser.
