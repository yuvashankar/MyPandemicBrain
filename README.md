# Accomplishments
- Designed and completed a twin-stick shooter from scratch in under 48 hours using Unreal Engine 4 Blueprints
- Successfully implemented a difficulty scaling system that accounts for all skill levels by rewarding skillful execution
- Modified enemy actor physics to simulate a friction-less icy surface.
- Implemented a scoring system that takes into consideration player's score multiplier
- Developed a UI that displayed all of the necessary information to the player
- Created minimal but effective training and tool tips to help the player understand how to play the game.

# Goals

The goals of this project was to:
- Develop and ship a game in under 48 hours.
- Adhere to the theme of "Joined Together"
- To make something fun!

# Developer Overview

Since this was my first GameJam, my personal goal was to attempt to complete and ship a game in the allotted time limit. My idea was to create a twin stick shooter as that way I would only have to deal with two dimensions rather than 3.

When the theme was announced my first idea was to have two characters controlled by two sticks on a controller. It seemed like a smart thing to do going by one of the winners of the Game Jam. Doing a bit of research , I saw that it was possible to do this, but when it was implemented in Unreal Engine 4.26 the system didn't work.

I tried to create two separate player models and then tried to have them be independently controlled by the controller. But it seems that they had patched out this functionality in later revisions of Unreal Engine. I'm sure it's possible, but not feasible to discover the solution in the 48 hours.

Participating in GameJams is all about improvisational coding, it's important not to get bogged down by set backs like this. Going back to the third requirement of "make something fun", I just played around with my character model, and discovered that it's incredibly fun to try and use the character model to knock some of the default boxes out of the player space.

Why not just make a game about that?

So I created a game where the character needs to use the outer-most model, which is a fighter ship, to knock the boxes out while they protect the inner-most model --- the air ship --- from taking damage.

A lot of the time was spent on scaling the difficult. Boxes are randomly spawned into the ring. The system linearly increases the speed at which the boxes spawn. Where the spawn rate is defined as:

``` 
SpawnDelay = max_spawn_delay - ((time_elapsed/100) x (max_spawn_delay - min_spawn_delay)) 

if `spawn_delay` is less than min_spawn_delay:
    spawn_delay = min_spawn_delay
```
 

So the spawn delay decreases linearly until it reaches the minimum spawn delay. This allows the players to learn the systems get hurt in a reasonable way, but it can soon get sadistic.

This difficult scaling can also be observed in the game's level where the opening to knock the boxes out will get smaller as you increase your "multiplier". The general idea is that the better you do, the harder the game gets, and the more points you receive. The goal is to survive as long as possible while racking up as many points as you can.

Increasing the gap of the object was accomplished by modifying the transform of one of the wall objects. The formula to scale the wall's width was:

```
wall_scale = min_scale + (multiplier/100) * (min_scale - max_scale)
```

The multiplier's range only goes between 1 and 100 so when the player is at max heat, the system is at it's narrowest making it the most difficult to knock the boxes out.

You increase your multiplier by scoring points, and it decrease by one every second.

If there was one thing that I would have liked to do a bit better in the future is to improve the UI experience. Nearing the end of the Game Jam, I realized that I had not taught the systems very well to new players. Which is why you may notice that the UI has a lot to desire. In the future I would like to go into a game jam with the start screen and end screen put together before hand. That way there's no wasted time attempting to shoehorn the items in later.

If you play the game you may notice that there is no sound, this is because the game for some reason did not build correctly. I find the Unreal Engine build system very difficult to work with. This coupled with the ungodly size of the final games, I would like to try Unity in the future for Game Jams.

The game is available on itch.io. You can download and play the game. I hope you enjoy it!
 
# Acknowledgments

This game used several assets in the creative commons domain. They are listed below. It's ironic that Sony has copyright claimed ownership of one of the songs, even though they are all in the free domain.
 
"Airship" by Poly by Google [CC-BY (https://creativecommons.org/licenses/by/3.0/)] via Poly Pizza (https://poly.pizza/m/dRpj4_t2keh)
"Spaceship" by Liz Reddington [CC-BY], via Poly Pizza
 
"Anti-Gravity Drone" by Adam Marc Williams [CC-BY], via Poly Pizza
 
Pop Sound: https://freesound.org/people/InspectorJ/sounds/411642/
 
Space Swwosh: https://freesound.org/people/GameAudio/sounds/220191/
 
Ouch Sound: https://freesound.org/people/Under7dude/sounds/163441/
 
Death Noise: https://freesound.org/people/MATRIXXX_/sounds/403296/
