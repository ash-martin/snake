# To clone this template:

Enter these commands into your bash terminal to clone the repository and delete the `.git/` folder:

```bash
git clone https://github.com/ash-martin/snake.git
rm -rf asd-template/.git
```

Then, rename the folder to the project name of your choice.

# Planning

_NOTE: Many of these steps reference the [Bouncing Box Project](https://jsbin.com/goyuhod/3/edit?html,output)_

Always start any programming task by clarifying what you want to do and then breaking it down into small steps. Small steps can get you just about anywhere if you’ve got enough time. If you get stuck, break it down smaller!

# Skills Practiced
- Separation of Concerns and Abstraction
- Keeping code organized between `initialization`, `core logic`, `helper functions` and `event handler` sections
- Controlling DOM elements with jQuery
- Managing data for DOM elements with Objects and Factory Function
- Managing a collection of Objects with an Array
- Iteration
- Initializing new DOM elements with jQuery

# Worksheet

Before beginning, complete the <a href="https://drive.google.com/open?id=1h9DBLktvwVCODaAn4vg5FKnbkbyYjLIMik5IMYMbhY0" target="_blank"> Snake Worksheet </a>

<img src="snake-visualization.png">

# Requirements

## The Board
**1) Think of the board as a 2-D grid of 20 pixel * 20 pixel squares.** 

For example If the board is `440` pixels wide and `440` pixels tall:
  - 22 columns along the x-axis
  - 22 rows along the y-axis
  
**2) Game items (the apple, each piece of the snake) must be positioned in intervals of 20 pixels.** 

For example, consider the conversions below:
```
snakeHeadColumn = 5;
snakeHeadX = 20 * snakeHeadColumn = 100

snakeHeadRow = 10;
snakeHeadY = 20 * snakeHeadRow = 200
```

## The Snake

**1) Each component of the snake must be an `{ Object }`**

**2) The entire snake's body must be represented as an `[Array]` of these `{Object}`s**
  - The first object in the Array is the "head" of the snake

**3) When the snake collides with the apple:**
  - A new DOM element is created and added to the board using jQuery.
  - A new snake `{Object}` is created and added to the snake `[Array]`
  
**4) The snake's head must continously move in 20 pixel intervals**
  - The head can move along either the x-axis (horizontally) or the y-axis (vertically), but never both (diagonally)
  - The user controls when the snake's head changes direction
  - The 2nd snake object follow the head, the 3rd follows the 2nd, etc… 

## The Apple
**1) The apple must be an `{Object}`**

**2) The apple's location is determined randomly and must be in an unoccupied, valid position.**
- valid: the apple's x/y coordinate must be a multiple of 20
- unoccupied: any part of the snake cannot already be there

**3) Each time the snake collides with the apple, the apple is moved to a new, random, unoccupied, and valid location**

**4) The number of apples eaten must be displayed**