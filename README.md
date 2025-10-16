The T-Rex Runner Game
This is a P5.js implementation of the classic Google Chrome T-Rex Runner game. The player controls a T-Rex that runs across a desert landscape, dodging obstacles and accumulating score.

How to Play
Start: The game starts automatically when loaded. The T-Rex is running, and the score begins to increase.

Jump: Press the Space Bar to make the T-Rex jump over obstacles (cacti).

Scoring: Your score increases over time as the T-Rex runs.

Game Over: The game ends if the T-Rex collides with an obstacle. The "Game Over" and "Restart" images will appear.

Restart: Click the Restart button (the circular arrow) to start a new game.

Game Features
Obstacles: Randomly generated cacti of six different types appear as obstacles.

Clouds: Clouds float across the sky for visual effect.

Speed: The game speed (the velocity of the ground and obstacles) increases as your score gets higher. The obstacle velocity is set to -(4 + 3 * score / 100).

Game States: The game uses two states: PLAY and END, to manage game logic, such as pausing movement and displaying the Game Over screen.

Collision Detection: Uses the obstacleGroup.isTouching(trex) function to detect collisions.

Files
sketch.js: Contains all the game logic, including:

Loading all images/animations in preload().

Setting up the game elements (T-Rex, ground, groups, score, game state) in setup().

The main game loop in draw(), which handles movement, gravity, scoring, collision detection, and game state transitions.

Functions for spawning clouds (spawnClouds()) and obstacles (spawnObstacles()).

A function to reset the game (reset()).

Image Assets: (Not provided, but referenced in sketch.js)

trex1.png, trex3.png, trex4.png: T-Rex running animation frames.

trex_collided.png: T-Rex image when the game ends.

ground2.png: The running ground image.

cloud.png: The cloud image.

obstacle1.png to obstacle6.png: Images for the different cactus obstacles.

gameOver.png: The Game Over text image.

restart.png: The Restart button image.

Technical Details
Platform: P5.js (JavaScript library for creative coding).

Game Loop: The draw() function runs continuously, managing the game state and updates.

Gravity: The T-Rex's jump is implemented using gravity, where trex.velocityY is continuously increased by 0.8.

Groups: P5.play's Group feature is used to manage multiple clouds and obstacles, making collision detection and bulk manipulation (like setting lifetime and velocity) easier.

Project Setup (How to run the game)
Ensure you have a P5.js environment set up (e.g., using the P5.js Web Editor, or a local server).

Place the sketch.js file and all required image assets in the correct directory.

Open the index.html file (which should link to the P5.js library and sketch.js) in a web browser.
