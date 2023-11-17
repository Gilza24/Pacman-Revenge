# Pac-Man Game

This Pac-Man game is a classic implementation using HTML5 canvas and JavaScript. It offers multiple levels, each presenting unique challenges such as avoiding ghosts, collecting good food for points, and dealing with bad food that reduces points.
For a good use of the game, i recommand to play on the Browser Chrome, some Browsers such as Safari slows down the game.

To create this game, i used OOP concepts to represent the elements within the game by using this link: 
https://openclassrooms.com/fr/courses/7133336-utilisez-des-design-patterns-en-javascript/7477066-consolidez-vos-bases-en-oriente-objet-avec-javascript

## Getting Started

To start playing the game, simply open the `index.html` file in a web browser. Click the "Start" button to initiate the game. Control Pac-Man's movement using the mouse. Additionally, press the "Escape" key to pause the game, and use "1" to resume or "2" to quit.

## Game Elements

### Pac-Man
- Main character controlled with the mouse.
- Collect good food to earn points.
- Avoid ghosts and bad food to prevent point deduction.

### Ghosts
- Enemies that move towards Pac-Man.
- Collision with a ghost results in the end of the game.

### Food
- Good food: Collect to earn points.
- Bad food: Avoid to prevent point deduction.

### Levels
- Multiple levels with increasing challenges.
- Introduces different types of food and enemies.

## Classes

- **Circle**: Basic circle element with position and collision detection.
- **Ghost (extends Circle)**: Ghost character with specific color and movement behavior.
- **PacMan (extends Circle)**: Player-controlled character with unique movement and drawing logic.
- **Food (extends Circle)**: Food items for Pac-Man to collect for points.
- **AliveFood (extends Food)**: Food items with dynamic movement.
- **ZigZagAliveFood (extends AliveFood)**: Food items with zigzag movement upon collision with walls.
- **ZigZagRandomSizeAliveFood (extends ZigZagAliveFood)**: Food items with random size changes over time.
- **Game**: Manages the game loop, user input, and initializes the current game level.
- **Level**: Represents a game level with specific challenges.
- **Levels**: Manages the progression of game levels.

## Gameplay Controls

- Use the mouse to control Pac-Man's movement.
- Press the "Escape" key to pause the game.
- Press "1" to resume the game or "2" to quit.

## Game Development Notes

- Implemented using HTML5 canvas and JavaScript.
- Each level introduces new challenges and features.
- Sound effects are used for various game events.

## Points developed in the game

### Done
- I Started out my project based on the content of the second module.
- In order to display the level number on the righ, i used the 2d context object fill text method.
- To give the player a nicer shape, I found inspiration to draw the main player and enemmies (ghosts) in the following link:
  http://www.java2s.com/example/javascript-book/pacman-and-ghost.html
- In this link i borrowed the logical code  of how the ghost chases Pacman. However, i had to add the logical code of when Pacman gets devoured by ghosts.
- Among all games states i only focused on pause state. In order to check that the game is in pause state, i setted the level object attribute named gamePaused at true or false when the user press the escape button. For the game over state i just popped up an "game over" message with the alert method and then refreshed the page with location.reload.
- In the game pause menu i listened the key 1 to resume game and the key 2 to quit the game. To resume the game i set the "game pause" attribute to false. To quit the game i popped up the quit game message and refreshed the game.
- For input fields, i used the HTML element input of type range as a coefficient of the speed of the alive ennemies.
- In your version, the balls (red ones) tooked the opposite version when it hits x axes and y axes walls. However, in my version i added a type of ball(orange ones) that when it hits the wall the speed and the trajectory becomes random.
- I also added a type of ennemy (yellow balls) which changes its size every 3 seconds.
- I added sound effects when starting the game, balls hittinh the hall so on...

### In The Future

As part of my plan to improve the game, i am planning to make Pacman shot the ghosts by eating a special ball
- For the other elements of the game i am planning on implementing a gravity functionnality that would make the enemmies go down on the screen when Pacman eats another special ball.


## License

This Pac-Man game is provided under the MIT License. Feel free to explore, modify, and distribute the game as needed.
