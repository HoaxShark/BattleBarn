## Welcome

In BattleBarn 2-4 players compete against one another in a frenzied top down shooter. With 4 different animals to play as, and power ups to mess up your friends, this game can constantly deliver new experiences.

The games last for a short amount of time letting you pick up and play during group gatherings really easily. With a focus on power ups debilitating your enemies, you get plenty of opportunities to annoy your friends!

Unique Selling Points;
1. Power ups that debuff your enemies!
2. Dark cartoony farmyard aesthetic.
3. Destructible environment.

Created by Gloomy Barracuda Studios a freshly formed group of 1st year students studying at Falmouth University.

### Video

[![BattleBarn Trailer](https://i.imgur.com/4etFEJ1.jpg)](https://youtu.be/rlgZfpDi7L8 "BattleBarn Trailer")

### Instructions

![BattleBarn Instructions](https://i.imgur.com/2qu7pWc.jpg)

### Screenshots

![Cow Shooting](https://i.imgur.com/TzvtRgB.png)

![4-player Map Night](https://i.imgur.com/WKQ0o9y.jpg)

![Scarecrow](https://i.imgur.com/fWaAr01.jpg)

![Goat Shooting](https://i.imgur.com/0xaChTW.png)

![2-player Map Day](https://i.imgur.com/miOqbS1.jpg)

![Scarecrow](https://i.imgur.com/2Cu1sPa.jpg)

### Blog - Adrian
Hi, I'm Adrian, I'm a programmer and I mainly worked on creating and implementing the different character shooting and ability mechanics. I also worked on the spawning system, made certain objects/obstacles destructible in the play space and helped integrate some of the sound effects. 

Not knowing Unreal very well or C++, I was quite slow at implementing things at the beginning of the project and as a result ended up mainly using blueprints to program the majority of the game. As the project progressed, I became more confident with Unreal and blueprints so managed to implement the majority of what the designers requested, even using C++ - in an albeit limited way - for some parts of the character mechanics.

We had a hard time using Unreal during the first few weeks and this seemed to sap morale amongst the team a bit. This led to me doing a lot of the core parts of our game which, given my lack of knowledge in the subject, means that alot of the game was made in a less that efficient manner. 

I admit that the need to have a functioning game after having had made such little progress in the first few weeks meant that I didn't necessarily have a focus on planning ahead for future systems after the core mechanics were at least working.

This unnecesarily complicated future systems, evidenced in the later stages of development when trying to devise a score system. A lot of my programming for the damage dealing system relied on each player detecting which character projectile was colliding with them, and then calculating the damage done to to that player being hit using a function specific to the projectile of the attacking player (such as HitByCow()) to lower the defending players health. This is all done individually in each character blueprint with every function originating in the base class BattlebarnPawn, from which each character BP inherits. 

![HitByCow function](https://i.imgur.com/GbYpE2e.png)
![HitByCow function BP](https://i.imgur.com/c6bjNub.png)

I think a better way of detecting damage and how players kill other players would have been to use casting or another method better suited that I wasn't aware of when making it. This meant it was very difficult when trying to determine which player killed another player, hence making a score system troublesome and require a lot of assistance to help create.

All in all I have learned a lot from this project and hope to improve upon my perhaps inefficient programming techiques in future projects.

### Blog - Beren
Hello, I'm another programmer, I worked on generating a UI with the main menu and the in game UI and helped with ability mechanics, unfortunately a lot of what I did at the start of the project didn't make it into the main game, I felt as though even though I had never worked with unreal I had been very productive at the start of the project, however due to some mistakes with version control and working on seperate builds much of what I had done at the start of the project never made it into the game. In my next project I feel as though I need to keep up my enthusiasm and work ethic throughout the project. I think in the next game I would enjoy working in C++ much more as I understand how C++ works with unreal much better. I have to commend Adrian for helping out and doing a substantial amount of the game.

The game was simple, however the biggest struggle for us was getting a spawn for 4 random charecters in all 4 corners. We also had a few issues where I had developed the mechanics for all 4 charecters, however due to a mistake on our charecter sheet I had developed them with 2 abilites and all with the same shooting mechanic, this was scrapped and a single mechanic was developed for all of the charecters. The first general idea for the game was to use a base C++ class and create children of that for all of the charecters this was another issue in that I had started to create many of the player mechanics in C++ classes however blueprints had been created as children of the main c++ class so this was also not used in the game.

At the start of the project there were many issues with version control with unreal due to intermediate folders. This ment that a few different builds had to be created, however after learning from a lecturer about builds and regenerating visual studio files we had much fewer issues.

### Blog - Ryan
My name is Ryan Clarke, I'm a first year programmer studying Computing for Games BSc at Falmouth University. The main area of BattleBarn that I focused on was the power ups and how they interact with the players.

The power ups are one of our main unique selling points, they were designed to be focused on weakening your enemies, instead of the more common type that would buff the player collecting it. We hoped this would create a fun way of annoying your friends while still giving you an advantage.

The game itself is fairly simplistic in the amount of mechanics that it has, each available character has a different way of shooting, one ability that they can use on cooldown and the power ups. The first two of these mechanics are fixed and don't change, the main aspect of the game bringing in different outcomes to each player, other than the players themselves, are the power ups. Considering this I believe the power ups really bring a lot of value to the game and I was happy to get to work on them. Below you can see a UML diagram of how the power up system works.

![HitByCow function BP](https://i.imgur.com/GNPSWWk.png)

The game started being designed in C++ and we made slow progress forward as the majority of our programmers, including myself, had not used C++ or Unreal before. The first part of the power ups that I worked on was the SpawningVolume, a box collider that could be put into the game and randomly spawn power ups across its volume. I used a tutorial that was shown to us during a lesson to help make this, and then turned it into a Blueprint so that it could be added easily into the level. I also made the base class for power ups in C++ in a similar way.

As progress with C++ was very slow given the resources available online, it ended up being more productive to swap to Blueprints and use these more frequently. I wasn't very keen on this idea, although I was struggling with C++, I have a lot more interest in learning how to work with it than Blueprints. But I went along with the plan and decided learning Blueprints will still be a useful skill and it does make our progression much quicker.

We kept to the idea of using base classes and children of those for the power ups and players, but past that the architecture of the game devolved into putting whatever we could into the Blueprints to get mechanics working. I used a hacky way of working with interfaces and message sending to pass the activation of the power ups, from the power up itself, to the players that needed it. It wasn't a very proud moment but it was working and felt innovative although maybe dumb. I would like to have done this a different way, I feel like given another go now I would at least place all the power up effects in the player base class so you don't have to change the variables in each player when wanting to change how long a power up lasts for!

Another change I would like to have made is writing the power ups and how they affect the player in C++ instead of using mostly Blueprints to cover the issue. Once I had learnt about ways of using casting I did go back through the power up blueprints, and change how some of the power ups work when checking what is collecting it and who it should effect in return. This was a much tidier way of doing it than using for loops and branches like I had used previously.

Overall working on the group project has been useful when it comes to learning about how unreal can interact with some C++ code but mainly how Blueprints work and can work with different things in Unreal. I look forward to the next project where I don't have to learn as much of the basic foundations and can hopefully build more sections using C++.

### Blog - Darren
N/A

