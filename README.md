# A-Pathfinder
Andy Le, Andytule
December 14, 2019

## About
- This program implements the A* search algorithmn and visualizes the shortest path from the top right corner to the bottom left corner. The user can draw out obstacles and mazes as well as reset and solve the grid. 
- Developed through the use of Javascript, HTML, and CSS

## Usage Guide
- By left clicking, you can create a wall on an empty node of the grid
- Left click and dragging will alow you to fill in a line of nodes
- Going over walls with left click again will undo the wall and return the node to an empty state
- Pressing the solve button will display the solved maze (if solvable) 
- Pressing the reset button will reset the maze
- Each color represents a different node state
  - Pink represents the start node
  - Dark Blue represents the end node
  - Black represents walls
  - Bright Blue represents the path way
  - Green represents the nodes that were checked while searching
  - Light/Faded Blue represents empty nodes

![Demo](https://user-images.githubusercontent.com/47620000/70857738-54000e80-1ec2-11ea-9f2e-f0ba32d0b1f2.png "Demo")

![Reset](https://user-images.githubusercontent.com/47620000/70857860-3f247a80-1ec4-11ea-901b-2253abdd476c.png "Reset")
