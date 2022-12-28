  # Y1 Winterconf 2022/23 - Workshop, Godot
  
  ## Objective:
  During this worktime: 
  - You will be intruduced to Game Development.
  - You will be using GDScript as a programming language.
  - You will program your player movement.
  - You will create your own Minigame.

<br>
<div align="center">
<img src="https://i.redd.it/4vepr95bye861.gif" width="640" height="360" />
</div>


## Instructions:
> Before we start, make sure you have godot open and ready for work!

1. Choose your [Character](https://drive.google.com/drive/folders/17heoqicF1QPqbZkdqBJTqS7rkZeMe7k_).
2. Choose your [Map](https://drive.google.com/drive/folders/1qKDc3ycTWMciUUyECka5DdPp5M8XxmWL).
<br>

3. Open Godot and in your **Game Folder** create 2 folders: `Map` and `Player`.
    - Drag your map and character into your folder.
    - In the **Scene Dock** click on import, Preset, 2D Pixel, Set as Default for 'Texture'.
    - Finally click Reimport!
<br>

4. In the **Scene Dock**, Click on the plus icon and add a Node and rename it to "World".  

<br>

5. Right click on `World` and attach a `Sprite` Child Node. 
    - Drag your map from the **Game Folder** to your `Texture` in the **Inspector**.
    - In the **Inspector** click on Region and make sure Enables is On.
    - At the bottom of your screen click on `TextureRegion`.
    - Click on `Snap Mode` and make sure it's set to `Grid Snap`.
    - Select the relavent parts of your map.
    - Build some obstacles for your player.
    - finalize your map structure.

<br>  

6. In the **Scene Dock** attach a `StaticBody2D` Child Node to your `Sprite`.
    - To the `StaticBody2D` attach some `CollisionShape2D` Child Nodes.
    - In the **Inspector** click on `Shape` and select `New RectangleShape2D`.
    - Make sure you covered your whole map with Collision Shapes.
  
<br> 

7. In the **Scene Dock** attach a `KinematicBody2D` Child Node to your `World`.
    - To the `KinematicBody2D` attach a `CollisionShape2D` Child Node.
    - To the `CollisionShape2D` attach a `AnimatedSprite` Child Node.
    - Scale your `CollisionShape2D` according to your Character.
    - Click on your `AnimatedSprite` and in the **Inspector** click on `Frames`, `New SpriteFrames`


<br> 

8.


## Bonus:

## Extra Resources:
[Lecture](https://docs.google.com/presentation/d/1dV9A2t-hab9TFk4qK4kSlH3Dy74iri7XSTFc9AFVvkY/edit#slide=id.g1bf1654ac85_0_357),
[Video](https://www.youtube.com/playlist?list=PL9FzW-m48fn2jlBu_0DRh7PvAt-GULEmd),
[Godot Documentation](https://docs.godotengine.org/en/stable/index.html).





