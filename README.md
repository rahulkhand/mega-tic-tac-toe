# mega-tic-tac-toe
Better than tic-tac-toe

The rules are similar to the classic tic-tac-toe with a few caviats. 

Here is some fundamental terminology used in the rules:
A **play** or **move** means to place a single X or O **marker** on the board.
A **string** is a continuous sequence of nine moves such that the first string starts at the first move of the game,
and every string thereafter starts on the move after the ninth move of another string.

This is your board space, also known as the **outer grid**.
![mega-tic-tac-toe-board](https://github.com/rahulkhand/mega-tic-tac-toe/blob/main/mega-tic-tac-toe-board.png)

Within each of the nine cells of the outer grid lies an **inner grid**, which also contains nine cells.
Here is an example of a legal board state with examples of regular markers and big markers. Note the straights underlying each big marker.
![move-examples](https://github.com/rahulkhand/mega-tic-tac-toe/blob/main/moves-examples.png)

Rules:
1. The X player goes first. The O player goes second. Both players alternate moves
2. Each valid play consists of placing an X or O in one of the nine sections of one of the nine inner-tac-tac-toe grids
3. The difference of the number of empty sections on any two inner grids must always be one or zero.
4. When a player plays a move, the section they played in is considered no longer empty
6. Every string must incorporate moves played in each of the nine inner grids
7. For every string, if the board were to be cleared of all moves except for those from the respective string
   then dragging all nine inner grids on top of each other would appear to yield a single inner grid with no empty spaces
8. When a player has a horizontal, vertical, or diagonal straight of three of their markers within an inner grid, they must place
   a big marker over the inner grid with their straight, filling in the entire cell of the outer grid.
9. If no legal moves exist for a player, they may ignore all rules constraining placement and place their marker in a vacant
   cell of any inner grid. In this case only, the move still counts towards the nine moves of its string, and the string is
   permitted to be abnormal where it might not abide by rule _6_ and/or _7_.
10. The first player who can create a horizontal, vertical, or diagonal straight of three of their big markers within the outer grid wins
