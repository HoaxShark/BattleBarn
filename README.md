## Welcome

In BattleBarn 2-4 players compete agaisnt one another in a frenzied top down shooter. With 4 different animals to play as, and power ups to mess up your friends, this game can constantly delivers new experiences.

The games last for a short amount of time letting you pick up and play during group gatherings really easily. With a focus on power ups debilitating your enemies you get plenty of opportunities to annoy your friends!

Created by Gloomy Baracuda Studios a freshly formed group of 1st year students studying at Falmouth University.

### Video and Instructions

[![BattleBarn Trailer](https://i.imgur.com/4etFEJ1.jpg)](https://youtu.be/rlgZfpDi7L8 "BattleBarn Trailer")
![BattleBarn Instructions](https://i.imgur.com/2qu7pWc.jpg)


### Blog - Adrian
Hi, I'm Adrian, I'm a programmer and I mainly worked on implementing the different character shooting and ability mechanics. I also worked on the spawning system and made certain objects/obstacles destructible in the play space. Not knowing Unreal very well or C++ I was quite slow at implementing things at the beginning of the project and as a result ended up mainly using blueprints to program the majority of the game. As the project progressed, I became more confident with Unreal and blueprints so managed to implement the majority of what the designers requested, even using C++ - in an albeit limited way - for some parts of the character mechanics. All in all I have learned a lot from this project and hope to improve upon my perhaps inefficienct programming techiques in future projects.

### Blog - Beren
Hello, I'm another programmer, I worked on generating a UI with the main menu and the in game UI and helped with ability mechanics, unfortunately a lot of what I did at the start of the project didn't make it into the main game, I felt as though even though I had never worked with unreal I had been very productive at the start of the project, however due to some mistakes with version control and working on seperate builds much of what I had done at the start of the project never made it into the game. In my next project I feel as though I need to keep up my enthusiasm and work ethic throughout the project. I think in the next game I would enjoy working in C++ much more as I understand how C++ works with unreal much better. I have to commend Adrian for helping out and doing a substantial amount of the game.

### Blog - Darren

### Blog - Ryan
My name is Ryan Clarke, I'm a first year programmer studying Computing for Games BSc at Falmouth University. The main area of BattleBarn that I focused on was the power ups and how they interact with the players.

The power ups are one of our main unique selling points, they were designed to be focused on weakening your enimies, instead of the more common type that would buff the player collecting it. We hoped this would create a fun way of annoying your friends while still giving you an advantage.

The game itself is fairly simlistic in the amount of mechanics that it has, each avaliable character has a different way of shooting, one ability that they can use on cooldown and the power ups. The first two of these mechanics are fixed and don't change, the main aspect of the game bringing in different outcomes to each player through, other than the players themselves, is the power ups. Considering this I believe the power ups really bring a lot of value to the game and I was happy to get to work on them.

The game started being designed in C++ and we made slow progress forward as the majority of our programmers including myself had not before used C++ or Unreal. The first part of the power ups that I worked on was the SpawningVolume, a box collider that could be brought into the game and randomly spawn power ups accross its volume. I used a tutorial that was shown to us during a lesson to help make this, and then turned it into a Blueprint so that it could be added easily into the level. I also made the base class for power ups in C++ in a similar way.

Progress with C++ was very slow and with the resources avaliable online, it ended up being more productive to swap to Blueprints and use these more frequently. I wasn't very keen on this idea, although I was struggling with C++, I have a lot more interest in learning how to work with it than Blueprints. But I went along with the plan and decided learing Blueprints will still be a useful skill and it does make our progression much quicker.

We kept to the idea of using base classes and children of those for the power ups and players, but past that the architecture of the game devolved into putting whatever we could into the Blueprints to get them working. I used a hacky way of working with interfaces and message sending to pass the activation of the power ups from the power up itself to the players that needed it. It wasn't a very proud moment but it was working and felt inovative although maybe dumb. I would like to have done this a different way, I feel like given another go now I would at least place all the power up effects in the player base class so you don't have to change the variables in each player when wanting to change how long a power up lasts for!

Another change I would like to have made is writing the power ups and how they effect the player in C++ instead of using mostly Blueprints to cover the issue. Once I had learnt about ways of using casting I did go back through the power up blueprints, and change how some of the power ups work when checking what is collecting it and who it should effect in return. This was a much tidier way of doing it than the for loops and branches that I had used previously.

Overall working on the group project has been useful when it comes to learning about how unreal can interact with some C++ code but mainly how Blueprints work and can work with different thing in Unreal. I look forward to the next project where I don't have to learn as much of the foundationary basics and can hopefully build more sections using C++.


### Markdown Gudie (will help with your blog posts)

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).
