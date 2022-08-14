# Accomplishments


- Created a Cherry Blossom particle effect system using Unreal Engine's Niagara Particle System
- Leveraged Blender to create a bespoke Cherry Blossom model.
- Created a custom texture that would react to the player's position allowing for easier conveyance of the system's functionality.
- Leveraged Blueprint Interfaces, Custom Events, and Event Dispatchers to create a scalable game in a limited amount of time.

# Developer Overview

This game was developed over the course of two weeks, with the main focus on building a game with a central theme correctly. My previous project, while a hack that got the job done was not very well put together, and I wanted to spend some time understanding Unreal Engine's Blueprint communication.

This game features almost all versions of Unreal Engine's Blueprint communication. For example:

- An object interface class that allows custom events to be triggered if implemented
- A one-to-all event dispatcher that allows multiple actors to react to a single event
- A custom event that does a one-to-one communication between the level and actor

 

I worked on the game in my spare time at a slower pace, because I wanted to learn about the game engine and how to correctly build something rather than creating spaghetti code.


This game was quite small in scope, press button to perform action, and I had the core functionality put together in about 1.5 weeks. Since I was done a bit earlier, and I conveyed as much information as I could, I decided to add a stretch goal of learning the Niagara Effects System to create the Sakura Cherry Blossom Effect in honor of Nujabes' Japanese origins.

Following the instructions outlined in this video I modeled a cherry leaf petal in Blender and added it into the Niagara Effects System.

This anecdote speaks to the positive effects proper software development has on a project. I was able to stay on the critical path, and create the code the right way.
 
I was able to make the addition with very little overhead. Adding the Niagara Effect system was just an order of having the effect blueprint bind to the Button Event Dispatcher and enabling itself when the user pressed the "Dopamine Button."
