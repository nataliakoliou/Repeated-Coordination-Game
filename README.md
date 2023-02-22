# Repeated Coordination Game

* The code implements a Repeated Coordination Game between 7 players using Q-Learning.
* Two actions: "Action[1]" and "Action[2]", and two types of players: "X" and "Y" are involved.
* The payoff of each player depends on the combination of actions chosen by him and his opponent, and the pair in which he is involved in a given round.
* The neighbors list specifies the pairs of players that are matched together in each round - each player may participate in multiple pairs depending on the size and structure of the network.
* The game is played repeatedly with a predefined number of episodes.
* Each player's Q-table is updated according to the rewards received during the moments of each episode.
* Exploration rate gradually decreases over the course of the game, in order to encourage players to exploit the game more often as the game progresses.
* Players' performance is graphed over time and the final actions & Q-values for each player are printed at the end of the game.

#### Functions of the code ####
* The "qlearning" function is the main function that orchestrates the game, calling the other functions as needed.
* During the game, the "game_print" function is responsible for printing the state of the game during each round of exploration and exploitation.
* The "graph" function is used to generate graphs that show, how the player's choices (actions) and rewards evolve over time.
* The "explore" and "exploit" functions select actions during exploration and exploitation phases of the game. 
* The "update" function updates the players' Q-tables based on the rewards received during a given round.
* The "get_opponent" function identifies the opponent for a given player.

## Prerequisites
The following python packages are required for the code to run:
* Python 3: https://www.python.org/downloads/
* NumPy: ```pip install numpy```
* Matplotlib: ```pip install numpy sklearn matplotlib```

**Alternatively:** you can download [requirements.txt](https://github.com/nataliakoliou/Repeated-Coordination-Game/blob/main/requirements.txt) and run ```pip install -r requirements.txt```, to automatically install all the packages needed to reproduce our project on your own machine.

## Conclusion
This code provides a good example of how Q-Learning can be used to simulate a multi-player game with dynamic rules and payoffs.

## Authors
Natalia Koliou & Konstantinos Chaldaiopoulos
