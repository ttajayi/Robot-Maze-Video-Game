# Maze Planet: Robot Maze Video Game

A maze-based video game developed in **C++** using Microsoft Visual Studio. Players control a robot navigating through a maze to locate hidden treasure while avoiding a pursuing monster.

The game features interactive movement, automatic navigation, backtracking, obstacle detection, and enemy movement behavior.

## Gameplay Demo

[Watch the gameplay demonstration](demo/gameplay.mp4)

## Features

- **Interactive Robot Movement:** Navigate through the maze using keyboard arrow keys while avoiding walls and obstacles.
- **Automatic Navigation:** Activate an automatic movement mode that follows a predefined sequence of directions.
- **Monster Pursuit:** A monster attempts to approach the robot using directional movement logic while avoiding maze walls.
- **Backtracking:** Return to the robot's previous position using a movement history system.
- **Treasure Detection:** Reach the designated treasure location to successfully complete the game.
- **Win/Loss Conditions:** Display victory or game-over messages based on whether the robot reaches the treasure or is caught by the monster.
- **File-Based Maze Loading:** Read maze layouts from external text files.

## Technologies Used

- **Language:** C++
- **Development Environment:** Microsoft Visual Studio
- **Graphics:** Custom Windows-based graphics library provided for coursework
- **Concepts:** Two-dimensional arrays, file I/O, functions, conditional logic, loops, movement history, and collision detection

## Game Controls

| Key | Action |
|---|---|
| Arrow Keys | Move the robot |
| A | Activate automatic navigation |
| B | Return to the previous position |
| Q | Quit the game |

## Maze Layouts

The project includes two maze configurations:

- `maze1a.txt` — Smaller maze (31 × 11)
- `maze2a.txt` — Larger maze (61 × 24), used by default

Maze layouts are stored as text files using the following symbols:

| Symbol | Meaning |
|---|---|
| `X` | Wall |
| `-` | Open pathway |
| `+` | Starting position |
| `$` | Treasure location |

## How It Works

**1. Maze Initialization**

The program reads a maze layout from a text file and stores its contents in a two-dimensional character array. It identifies the starting position and treasure location before rendering the maze.

**2. Player Movement**

The robot responds to keyboard inputs. Before moving, the program checks the maze layout to prevent the robot from passing through walls.

**3. Monster Movement**

The monster begins at a randomly selected valid position and attempts to move toward the robot. Its movement logic prioritizes directions based on the relative positions of the two characters while checking for walls.

**4. Automatic Navigation**

Automatic mode processes a predefined sequence of movement commands. This provides automated movement through the maze rather than dynamically calculating a shortest path.

**5. Backtracking**

The game stores previous robot positions in a movement history, allowing the player to return to an earlier position.

**6. Game Completion**

The game displays a victory message when the robot reaches the treasure and a game-over message if the monster catches the robot.

## Running the Project

### Requirements

- Windows operating system
- Microsoft Visual Studio with C++ support
- Course-provided `library.h` and `library.obj` graphics dependencies

### Setup

1. Download or clone the repository.
2. Open the C++ project in Visual Studio.
3. Obtain the required course graphics library files and configure them for compilation and linking.
4. Ensure `maze2a.txt` is accessible from the program's working directory.
5. Build and run the application.

**Note:** The graphics library was provided for coursework at the University of Miami and is not included in this public repository. The project cannot be built independently without the required library dependencies.

## Project Background

Developed as part of **ECE 118: Introduction to Programming** at the University of Miami.

The project provided practical experience implementing interactive gameplay mechanics, working with two-dimensional arrays, managing program state, reading external files, and developing movement behavior in C++.
