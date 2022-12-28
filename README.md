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

### Part 1 : Designing your game
 - Choose your [Character](https://drive.google.com/drive/folders/17heoqicF1QPqbZkdqBJTqS7rkZeMe7k_).
 - Choose your [Map](https://drive.google.com/drive/folders/1qKDc3ycTWMciUUyECka5DdPp5M8XxmWL).
<br>

### Part 2 : Importing to Godot
 - Open Godot and in your **Game Folder** create 2 folders: `Map` and `Player`.
 - Drag your map and character into your folder.
 - In the **Scene Dock** click on import, Preset, 2D Pixel, Set as Default for 'Texture'.
 - Finally click Reimport!
<br>

### Part 3 : Creating the main Node
 - In the **Scene Dock**, Click on the plus icon and add a Node and rename it to "World".  

<br>

### Part 4 : Creating your Map
 - Right click on `World` and attach a `Sprite` Child Node. 
 - Drag your map from the **Game Folder** to your `Texture` in the **Inspector**.
 - In the **Inspector** click on Region and make sure Enables is On.
 - At the bottom of your screen click on `TextureRegion`.
 - Click on `Snap Mode` and make sure it's set to `Grid Snap`.
 - Select the relavent parts of your map.
 - Build some obstacles for your player.
 - finalize your map structure.

<br>  

 - In the **Scene Dock** attach a `StaticBody2D` Child Node to your `Sprite`.
 - To the `StaticBody2D` attach some `CollisionShape2D` Child Nodes.
 - In the **Inspector** click on `Shape` and select `New RectangleShape2D`.
 - Make sure you covered your whole map with Collision Shapes.
  
<br> 

### Part 5 : Creating your Character & Animations
 - In the **Scene Dock** attach a `KinematicBody2D` Child Node to your `World`.
 - To the `KinematicBody2D` attach a `CollisionShape2D` Child Node.
 - To the `CollisionShape2D` attach a `AnimatedSprite` Child Node.
 - Scale your `CollisionShape2D` according to your Character.
 - Click on your `AnimatedSprite` and in the **Inspector** click on `Frames`, `New SpriteFrames`.
 - Click on `SpriteFrames` at the buttom of your screen.
 - Change Default to `Idle` and add your `Idle` frames.
 - Add `New Animations` for Running, Jumping, Falling.


<br> 

### Part 6 : Coding your Character's movement
 - Right click on your `KinematicBody2D` and attach a `Script` to it and click `Load`.
 - Let's define our **Key Constants**:
  ```gdscript
  extends KinematicBody2D
  
  const UP = Vector2()
  const GRAVITY = 1200
  const JUMP_HEIGHT = -700
  const SPEED = 200
  ```
 - Let's define our **Main Physics function** take the following code and complete it:
 
 ```gdscript
  func _physics_process(delta):
    # Set up Gravity
    if Input.is_action_pressed("ui_right"):
      # Move player to the right
      # Play the suiting animation
      
    elif Input.is_action_pressed("ui_left"):
      # Move player to the left
      # Play the suiting animation
      
    else: 
      motion.x = 0 
      # Play the suiting animation
      
    if is_on_floor():
      # Set user input for jump 
      # Play the suiting Animation
      
    else:
      # Play the suiting Animation
      
    # Complete the code to play the falling animation when the player is falling 
      
      
   motion = move_and_slide(motion, UP)
  ```

<br>
<p align="center">
<h2> Good Job! Remember to show your wonderful work to your Instructors and TAs :partying_face: <h2>
</p>
<br>
 
## Bonuses:
 - Make your `Character` move using **W,A,S,D**
 - Add more `Levels` to your game by creating more `Scenes`.
 - Move between your `Levels` once the level is complete.
 - Have an `Automatic Tile Map` to quickly create more `Levels`.
 - **GO CREATIVE AND EXPLORE**
<p float="center">
  <img src="https://i.pinimg.com/originals/16/94/5c/16945c320155f09714d53df27c81370a.gif"/>
</p>
 
## Extra Resources:
[Lecture](https://docs.google.com/presentation/d/1dV9A2t-hab9TFk4qK4kSlH3Dy74iri7XSTFc9AFVvkY/edit#slide=id.g1bf1654ac85_0_357),
[Video](https://www.youtube.com/playlist?list=PL9FzW-m48fn2jlBu_0DRh7PvAt-GULEmd),
[Godot Documentation](https://docs.godotengine.org/en/stable/index.html).





