---
layout: page
title: Battle of the river
description: A shooting and dodge game
img: /assets/img/projects/battle_of_the_river/botr_homescreen.png
importance: 1
github: https://github.com/ricardogpinho/BattleOfTheRiver
---

This game was conceived during my *Academia de Código* bootcamp.
From the 20 alumni, 4 groups of 5 elements were arranged and the challenge assigned to all groups was to develop a *JAVA* game using the *simpleGFX* libray, in the span of a week, in our spare time, mostly at the end of the day, at the end of the lectures.
My group was composed by [Adriana](https://github.com/AdrianaAC), [João](https://github.com/joaopinheiro10), [Neide](https://github.com/NeideMargarido), [Rui](https://github.com/ruipatricio72) and me.

***Battle of the river*** born as an idea on our very first day of the project. Many other game ideas were considered, but we had to make a decision quickly and we decided to tackle this one. The game would consist in two characters, one controlled by the player and the other one by the CPU, each one in is own battlefield, shooting arrows at the other. Potions of health and venom would spawn across both fields. The first taking all the opponent's health points would win.

Some guidelines, scheduling, graphics and game mechanics were thought and first assigned to the different members of the team.
We started by deciding the screen size, the graphical objects and then we began implementing the very first mechanics of the game.
Quickly we gathered most of the graphics we needed and assembled the map of the game.
<div class="text-center">
    <img src="/assets/img/projects/battle_of_the_river/resources/map-1.png" class="img-fluid rounded z-depth-1" width="50%" height="50%">
    <div class="caption">
        Battleground map
    </div>
</div>

<div class="d-flex justify-content-center">
    <div>
        <img src="/assets/img/projects/battle_of_the_river/resources/shootVerde1.png" class="img-fluid rounded">
    </div>
    <div>
        <img src="/assets/img/projects/battle_of_the_river/resources/shootVermelho2.png" class="img-fluid rounded">
    </div>
    <div>
        <img src="/assets/img/projects/battle_of_the_river/resources/deadVerde1.png" class="img-fluid rounded">
     </div>
    <div>
        <img src="/assets/img/projects/battle_of_the_river/resources/deadVermelho2.png" class="img-fluid rounded">
     </div>
    <div>
        <img src="/assets/img/projects/battle_of_the_river/resources/tree4_3x3.png" class="img-fluid rounded">
    </div>
    <div>
        <img src="/assets/img/projects/battle_of_the_river/resources/tree6_1x1.png" class="img-fluid rounded">
    </div>
    <div>
        <img src="/assets/img/projects/battle_of_the_river/resources/potionHP.png" class="img-fluid rounded">
    </div>
    <div>
        <img src="/assets/img/projects/battle_of_the_river/resources/venomPotion.png" class="img-fluid rounded">
    </div>
</div> 
<div class="caption">
    Some of the game objects
</div>

With graphics mostly settled, we began working on the game input, character movements and movement restrictions.
With that done, was time to implement shooting. This was tricky... because the arrows would have to spawn on key-press trigger and then disappear at hitting a character, object or reach the end of the map. It required a linked list, but we manages it.

That implemented, was time for making the autonomous player move and shoot as well. With some logic and randomness generation this was also achieved.

At two days from the deadline we were yet to implement the scoring bar. It took almost an entire day but that was also accomplished.

At last, on the very last day, just before the deadline, we were still resolving some game bugs, implementing the menu screen, the restart-game option and the final-game screens. This job was divided across the entire team and, at last, we managed to put our game together just in time.    

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/projects/battle_of_the_river/homescreen.png' | relative_url }}" alt="" title="example image"/>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/projects/battle_of_the_river/gameplay_1.png' | relative_url }}" alt="" title="example image"/>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/projects/battle_of_the_river/endscreen.png' | relative_url }}" alt="" title="example image"/>
    </div>
</div>
<div class="caption">
    On the left, the start screen. In the middle, in-game gameplay. On the right, the end game screen.
</div>

Here is a bit of the gameplay, I lost this round.

<div class="d-flex justify-content-center">
<video controls class="z-depth-3 embed-responsive-item">
    <source class="embed-responsive-item" src="/assets/img/projects/battle_of_the_river/botr_gameplay.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>
</div>