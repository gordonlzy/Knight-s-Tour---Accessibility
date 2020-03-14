# Knight-s-Tour---Accessibility
A solution to the problem Knight's Tour by using the method of accessibility.
All 64 spots on the chessboard have been assigned a value of accessibility based on the number of spots that can access that spot.
The strategy is to access the spots that have the lowest accessibility possible each time.

Board.java
This class has instance variables currentFile, currentRow that determines the current spot; boxes which is the array containing the spots; and accessibility index of each spot.

Methods implemented:
- isCurrentIndex() -> check if the given box(file, row) is the currentIndex
- resetBoard() -> reset the board and its accessibility to their initial states
- printBoard() -> print the board and accessibility of each spot side by side
  - printFile() -> print each file of a selected row
  - printRowAccessibility() -> print the accessibility of each file in the row

Spot.java
This class consists of instance variables file and row and methods to get and set the variables.

Knight.java
This class has methods that allow a knight to be placed and moved, occupy and alter the accessibility of spots.

Methods implemented:
- start() -> initialize first move, occupy and change accessibility based on the first move
- move() -> from the list of possible moves, select the moves with the smallest accessibility, occupy and change the accessibility of the selected spot
- occupySpot() -> set the spot as occupied, update currentFile and currentRow
- changeAccessibility() -> change the accessibility the spots affected after a spot is occupied
- possibleMove() -> return a list of possible moves based on the current spot of the knight

KnightsTour.java
This class contains the main method. It creates two objects of class Board and Knight and starts the knight's tour.
