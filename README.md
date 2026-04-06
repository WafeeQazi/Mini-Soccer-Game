---------------------------------------------------------------------------------------------------------------------------------------
How to Play
---------------------------------------------------------------------------------------------------------------------------------------
  1. Move your player with the arrow keys.
  2. Pick AI opponent difficulty from the dropdown menu.
  3. Score by getting the ball into the opponent’s goal.
  4. Watch the red line coming from the AI, it shows where the AI is aiming, so you can plan your moves.
  5. The game lasts 60 seconds.
  6. Click Restart Game anytime to play again.

---------------------------------------------------------------------------------------------------------------------------------------
Development Progress:
---------------------------------------------------------------------------------------------------------------------------------------
Day 1: I got the basics up and running. I made the buttons respond to the player properly. It was fun seeing the player finally move.

Day 2: I got the ball to move. It isn't done yet, but I have an idea for how it should interact with the player and AI.

Day 3: I got the player and ball to interact, and now players can push the ball around.

Day 4: I made an AI opponent which can push the ball around. It can’t aim just yet, but it is able to “dribble” the ball.

Day 5:  I added a scoring system through which the player and opponent can score on each other and gain points. I don’t have a display system for the scores yet, but the reset mechanism after each goal has been built.

Day 6: I added a 60 second timer for each game. The kickoff system is much better too, and now gives the player 3 seconds before each kickoff to think and strategize.

Day 7: The AI got smarter! I updated the AI so that it doesn't go in a straight line, and its direction of kicking varies. It is still very simple and easy to beat, so I’m planning on how I can make it better. A halfway line was also added.

Day 8: I fixed some bugs where players or the ball would end up in the corner, along with making the AI’s kicks a bit stronger, so that it can kick farther. There seem to be a lot of new bugs though, so I will have to fix those as well.

Day 9: I spent a lot of time fixing bugs, then I polished the visuals by adding white borders around the green field, and added a goalpost, along with a halfway line. I adjusted AI targeting to be more precise, towards the goal post. 

Day 10 (Final Day): Fixed AI push bugs and made everything feel smoother and fairer. I added a little AI target line so you can see what it’s thinking, updated the AI’s kicking pattern, and also created 3 different difficulty modes. You can enjoy a proper challenge now!

---------------------------------------------------------------------------------------------------------------------------------------
Object/Function            | Description
---------------------------------------------------------------------------------------------------------------------------------------
humanPlayer                | Represents the player controlled by arrow keys. Tracks position, speed, and radius.
computerAI                 | Opponent AI player. Moves toward the ball and pushes it with cooldown.
soccerBall                 | Ball object. Tracks position, velocity, radius, and color.
keysPressed                | Object storing which keys are currently pressed for movement.
scores                     | Tracks player and AI goals.
remainingTime              | Game timer in seconds.
isKickoff                  | Boolean indicating whether a kickoff is in progress.
kickoffTimer               | Countdown for kickoff in seconds.
aiPushCooldown             | Prevents AI from continuously pushing the ball every frame.
currentAIDifficulty        | Difficulty level: easy, medium, hard. Affects AI speed and push randomness.
updateScoreAndTimer()      | Updates HTML scoreboard and timer display.
movePlayer()               | Moves player based on arrow keys and keeps inside boundaries.
moveAI()                   | AI movement logic. Dribbles around the player and approaches the ball.
moveBall()                 | Updates ball position, applies friction, handles wall collisions.
checkCollision(obj)        | Handles ball–player/AI collision and “push” physics.
checkGoal()                | Detects if the ball entered a goal and updates scores, triggers kickoff.
startKickoff()             | Resets positions and starts a 3-second countdown.
resetPositions()           | Puts all players and ball back to starting positions.
drawCircle(obj, shadow)    | Draws a circle (player, AI, or ball) on canvas, optional shadow.
draw()                     | Handles all visual elements: field lines, kickoff countdown, AI line, ball shadows, Game Over overlay.
gameLoop()                 | Main animation loop calling all move, collision, and draw functions each frame.
---------------------------------------------------------------------------------------------------------------------------------------
