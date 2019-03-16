---
layout: default  
--- 

# Platformer

This is the second project for CS 5850.

A implementation of the classic platformer game using C++ and SDL2 Libraries

## Team:
Created by Fan Ling, Hao Tian, Wendi Zhang

## Documentations and Download
[Link towards documentation](https://flynn2016.github.io/platformer_doc)

[Link towards download](https://troyprag816gmailcom.itch.io/sdl-platformer)

#### Install Instruction:  
Platform: MacOS

Download through the link provided on the website. Make sure you have SDL2, SDL2_image, SDL2_mixer and  SDL2_ttf in your library. Run main to open the game in terminal. Run sprite_editor to test the sprite editor and run tile_editor to test the tile editor.

## Post Mortem 

In the second project, we built our game based on the framework setup in the first project. We introduced many new components like character physics
2d collision, AI movement etc. Many things are improved, for example, game logics are more organized and are where they should be. We were going to use
alpha blend to achieve transparent texture effect. But due to the time limit and effort, we gave up on that idea. Given more time, we would like to achieve the freedom to adjust the alpha value of any texture. 

Also one major bad decision made during the project is we chose a sprite sheet that is not transparent. And we realized it is a problem too late to overhaul our project. Two problems emerged from this decision. First, our sprite editor and tile editor are far from genetic like Unity or other game engine. Switching to another sprite sheet after already establishing most of the game takes a lot of rework. The second problem is sprites would overlay each other show the ugly background on top of each other. So next time we would be mindful to use a transparent background sprite sheet.

##Special Feature
So our special feature is the animation of the key at the end . We wrote the whole package of Unity-like transform: position, rotation, scale, even the parent-children relationship. Just like in Unity you can use Animator to create animation based on the transform of the gameobjects. We created a little simple animation of key movement using our transform package. It can do more than just rotating a key, for example, it can let a programmer animate different character movement with separate body part using just code so they don’t have to rely on art people to finish drawing hundreds of frame of texture.  Unfortunately, due to time limit we can not show it in the game, but I believe the idea is there. 

##Other Notes:
You can toggle the display of fps at the top of the GameManager.h file
And also we did not forget about the background. Like we said in the post mortem, we realized the spritesheet should have a transparent background too late. Right below the fps toggle, you can see there is a background toggle. Set it to true, you can view the background with the hideous square sprite.


### Video
<iframe width="560" height="315" src="https://www.youtube.com/embed/_w32w-XguGk" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


### ScreenShots

![ScreenShot_1](./Image/image_1.png)

![ScreenShot_2](./Image/image_2.png)

![ScreenShot_3](./Image/image_3.png)


