
# Simple chess ai

![Image of chessai](https://drive.google.com/uc?id=19zoO9s76ifxuY78ABn_kZyNIAHUk-WI7)

this is a simple chess ai program which is built up based on chess.js api

### How computer plays chess?

In simple words, computer plays chess based on calculations of all possible outcomes after making a particular move and then finally choosing the best move.

### step 1:
#### Create a tree of all possible moves possible at each turn
* for the first turn if the computer chooses white
* first moves possible are by `8 pawns + 2 knights` which is equal to	`8*2 + 2*2=20` possible moves by computer
* in response the `opp player can also make 20 possible moves`
* (IT NOT JUST CALCULATES ITS OWN MOVES BUT ALSO THE OPP PLAYER'S MOVES)
* and then evaluate(weights/marks) each move and choose the best one
* thus for starting two moves in the game '1 by computer','1 by opp player' we have `20*20=400 possible cases`/outcomes of different moves(to choose from)
* as the number of steps increases the nubmer of possible moves increases vastly
* based on this it makes a huge tree of all those possible moves
### step 2:
#### Use evaluation function
* many evaluations like kings vulnerability, control over center e.t.c are all calculated and taken under consideration
### step 3:
#### Apply minimax algorithm
* apply minimax algorithm on the simplified tree(starting from the bottom)
* each level on the tree is considered as payers turns,one turn after the other
5th level-`comp`--choose max score
4th level-`opp`---min score
3rd level-`comp`--max score
`assumes that best moves are made by opp`
`assumes worst moves made by computer itself`
