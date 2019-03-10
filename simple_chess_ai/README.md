
# Simple chess ai

![Image of chessai](https://drive.google.com/uc?id=19zoO9s76ifxuY78ABn_kZyNIAHUk-WI7)

this is a simple chess ai program which is built up based on chess.js api

### How computer plays chess?

In simple words, computer plays chess based on calculations of all possible outcomes after making a particular move and then finally choosing the best move.

#### step 1:

* create a tree of all possible moves possible at each turn
* for the first turn if the computer chooses white
* first moves possible are by `8 pawns + 2 knights` which is equal to	`8*2 + 2*2=20` possible moves by computer
* in response the `opp player can also make 20 possible moves`
* (IT NOT JUST CALCULATES ITS OWN MOVES BUT ALSO THE OPP PLAYER'S MOVES)
* and then evaluate(weights/marks) each move and choose the best one
* thus for starting two moves in the game '1 by computer','1 by opp player' we have `20*20=400 possible cases`/outcomes of different moves(to choose from)
* as the number of steps increases the nubmer of possible moves increases vastly
* based on this it makes a huge tree of all those possible moves
