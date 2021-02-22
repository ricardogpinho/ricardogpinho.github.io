---
layout: page
title: Car Crash
description: An experimental non-controllable game 
img: /assets/img/projects/car_crash/car_crash_ingame_scrnshot_1.png
importance: 2
gitlab: https://gitlab.com/ricardogpinho/my_exercices/-/tree/master/car-crash
---

This game is a simple project written in *JAVA* with the intuit of getting familiar with the *lanterna* library.
I only had one weekend to put it together and it was part of my *Academia de Código* bootcamp.

A base code was provided and it was asked to us to draw the cars (small rectangles) on the display and make them move in a minimal realistic way. If the cars would crash, they had to stop moving. Different variety of cars were required, cars that would move at different speeds and have different proprieties. The following minimum car types were required:
* Normal cars only with different speeds
* A Tank that would never crash
* An ambulance that would fix crashed cars

Once this requirements were met, we were allowed to be creative and implement whatever we wanted on top of it.
I went a bit further an created a route system for every car, and also I made a *Tesla* type car that would avoid crashing. Almost...

The route system consists in every car requesting it's own new route once it reaches it's destination, by getting it's current grid position, asking for a final position and creating an entire path from it's current to final position. This can be witnessed in the Tesla movement, in which I drew the route on the display for us to be able to see what's going on.

The Tesla is capable to avoid accidents, but there are occasions it can crash, specially against another equally fast cars. I couldn't solve this within the time I had to finish the project.

A demo follows.
   
<img src="/assets/img/projects/car_crash/car_crash_gameplay.gif" class="img-fluid">