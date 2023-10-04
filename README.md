# mega-tic-tac-toe
Better than tic-tac-toe

The rules are similar to the classic tic-tac-toe with a few caviats. 

Here is some fundamental terminology used in the rules:

* This is your board space, also known as the **outer grid**.
![mega-tic-tac-toe-board](https://github.com/rahulkhand/mega-tic-tac-toe/blob/main/mega-tic-tac-toe-board.png)

* Within each of the nine cells of the outer grid lies an **inner grid**, which also contains nine cells.
Here is an example of a legal board state with examples of regular markers and big markers. Note the **straights** underlying each big marker.
![move-examples](https://github.com/rahulkhand/mega-tic-tac-toe/blob/main/moves-examples.png)

* A **play** or **move** means to place a single X or O **marker** on the board.
* A **big marker** denotes that no more moves can be played in the inner grid that is being **covered**. 
   Essentially the player has captured that cell of the outer grid.
* A **string** is a continuous sequence of moves such that the first string starts at the first move of the game,
   and every string thereafter starts on the move after the last move of another string.
* The first string of the game will have nine moves in it, or a **length** of nine. When a big marker is placed on the board, the length
  of every string started thereafter decreases by one.

Rules:
1. The X player goes first. The O player goes second. Both players alternate moves
2. Each valid play consists of placing an X or O in one empty section of one of the nine inner-tac-tac-toe grids when it is not covered.
3. The absolute difference of the number of empty sections on any two inner grids that are not covered must always be one or zero.
4. When a player plays a move, the section of the inner grid they played in is considered no longer empty
5. Every string must incorporate a move played in each inner grid that is not covered before the aforementioned move is played.
6. For every string, if the board were to be cleared of all moves except for those from the respective string
   then dragging all nine inner grids on top of each other would have no moves overlapping each other.
7. When a player has a horizontal, vertical, or diagonal straight of three of their markers within an inner grid, they must immediately
   place a big marker over the inner grid that contains their straight, filling in the entire cell of the outer grid.
8. If no legal moves exist for a player, they may ignore rule _6_ but still must adhere to rule _5_. In this case only, the move still counts
   towards the length of its string, and the string is permitted to be abnormal where it will not abide by rule _6_.
9. The first player who can create a horizontal, vertical, or diagonal straight of three of their big markers within the outer grid wins
