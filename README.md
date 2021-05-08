# Cannonhead-Clash
A multiplayer game coded in C that runs on [CPUlator](https://cpulator.01xz.net/?sys=arm-de1soc). The game uses double buffering to display smooth visuals and animations on a VGA frame buffer. Additionally, the PS/2 keyboard is used for input. It generates interrupts which are dealt with accordingly to produce the needed output. 

This project was created for ECE243 which is a course at the University of Toronto on computer organization. As part of the course guidelines, the source code cannot be publicly shared, howvever, detailed description and gameplay images are given below. 

**Note: The game uses the PS/2 Keyboard typed input for all user interaction and gameplay**

## Menu Screen
Cannonhead Clash is a two player game where the objective is to hit the opposing player with a bomb, without falling into the water underneath a platform that the player is placed on.

- A menu screen is initially displayed that allows the user to select a level and the number of points needed for one of the players to win the game
  - The up and down arrow keys can be used to move the selection arrow and the spacebar can be used to change the level or number of points to win 
  - There are five different levels that the user can choose from and the points to win can range from one to five with one being the default option for both
  - To start the game, the spacebar must be pressed with the selection arrow at “PLAY” 

![Main Screen](/images/gameplay.jpeg | width = 100)

## Levels 
There are five differnt levels that the user can choose from (they are not in order of difficulty). 

Level 1                          |  Level 2                          |  Level 3                           
:-------------------------------:|:---------------------------------:|:----------------------------------:
![Level 1](/images/level1.PNG)   |  ![Level 2](/images/level2.PNG)   |  ![Level 3](/images/level3.PNG)    

Level 4                           | Level 5
:-------------------------------:|:---------------------------------:
![Level 4](/images/level4.PNG)    | ![Level 5](/images/level5.PNG)

## Controls
Once the user selects to play, the specified level is loaded and the two players can be controlled user the following key:  

|                 | Move Left    | Shoot       |  Move Right 
|----------------:|:------------:|:-----------:|:------------:
| **Player One**  | [A]          | [W]         | [D]  
| **Player Two**  | [←]          | [↑]         | [→]           
 
The players can automatically move up or down a level within a one block range. 

![Controls](/images/controls.jpg)

## Gameplay 
- The bombs can destroy the platform blocks if they do not hit a player and a player wins a point if the opposing player is:
  - Hit with a bomb or 
  - Falls off a platform block and into the water 
- The respective score for each player is displayed and updated at the bottom of the platforms. 

Once one of the players reaches the number of points to win, selected at the start of the game, the game ends. The winner is displayed for a couple seconds and the menu screen is displayed where the user can choose the settings to play at again. 

