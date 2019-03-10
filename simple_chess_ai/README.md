
# Simple chess AI

![Image of chessboard](https://drive.google.com/uc?id=19zoO9s76ifxuY78ABn_kZyNIAHUk-WI7)

* This is a simple chess ai application based on opensource chess.js API

### How computer plays chess?

* computer plays chess based on calculations of all possible outcomes after making a particular move and then finally choosing the best move.

### step 1:
### create a tree of all possible moves
* computer plays chess based on calculations of all possible outcomes after making a particular move and then finally choosing the best move.
* for the first turn if the computer chooses white then first moves possible by `8 pawns + 2 knights`
* which is equal to	`8*2 + 2*2=20` possible moves by computer
* in response the `opp player can also make 20 possible moves` for his first move
(IT DOESN'T JUST CALCULATES ITS OWN MOVES BUT ALSO THE OPP PLAYER'S MOVES)
* then evaluate(weights/marks) each move and choose the best one
* thus for starting two moves in the game 1 by computer,1 by opp player we have `20*20=400 possible cases`/outcomes of different moves(to choose from)
* as the number of steps increases the number of possible moves increases vastly
* based on this it makes a huge tree of all those possible moves

### step 2:
### Use evaluation functions
* many evaluations like king's vulnerability ,control over center e.t.c are all made(calculated) and taken under consideration for the next move

### step 3:
### Apply minimax algorithm
* apply minimax algorithm on the simplified tree(starting from the bottom)
* each level on the tree is considered as players turn one after the other
* 5th level-`comp`-choose max score
* 4th level-`opp`--min score
* 3rd level-`com`--max score ...
* `assumes that best moves are made by opp`
* `assumes that worst moves are made by computer itself`
