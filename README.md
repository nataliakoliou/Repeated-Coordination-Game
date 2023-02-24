# Repeated Coordination Game

The code implements a Repeated Coordination Game between 7 players using Q-Learning, for the purpose of reaching some Nash Equilibrium point.
* Two actions: "A1" and "A2", and two types of players: "X" and "Y" are involved.
* The payoff of each player depends on the combination of actions chosen by him and his opponent, and the pair in which he is involved in a given round.
* The neighbors list specifies the pairs of players that are matched together in each round - each player may participate in multiple pairs depending on the size and structure of the network.
* The game is played repeatedly with a predefined number of episodes.
* Each player's Q-table is updated according to the rewards received during the moments of each episode.
* Exploration rate gradually decreases over the course of the game, in order to encourage players to exploit the game more often as the game progresses.
* Players' performance is graphed over time and the final actions & Q-values for each player are printed at the end of the game.

### Important Functions in the Code ####
* **qlearning:** the main function that orchestrates the game, calling other functions as needed.
* **game_print:** is responsible for printing the state of the game during each round of exploration and exploitation.
* **graph:** is used to generate graphs that show, how the player's choices (actions) and rewards evolve over time.
* **explore & exploit:** select actions during exploration and exploitation phases of the game respectively. 
* **update:** updates the players' Q-tables based on the rewards received during a given round.
* **get_opponent:** identifies the opponent for a given player.

## Prerequisites
The following python packages are required for the code to run:
* Python 3: https://www.python.org/downloads/
* NumPy: ```pip install numpy```
* Matplotlib: ```pip install numpy sklearn matplotlib```

**Alternatively:** you can download [requirements.txt](https://github.com/nataliakoliou/Repeated-Coordination-Game/blob/main/requirements.txt) and run ```pip install -r requirements.txt```, to automatically install all the packages needed to reproduce our project on your own machine.

## Conclusion
This code provides a good example of how Q-Learning can be used to simulate a multi-player repeated game with dynamic rules and payoffs. Users are encouraged to modify the input data: "types", "payoff" or "neighbors", to observe the impact on the final convergence to Nash Equilibrium.

Here are some suggestions:
```python
# Change the types of players in the game, modify each type's payoff matrix, or edit the way players communicate with each other
9   types = ["X", "X", "X", "Y", "Y", "Y", "Y"]
10  payoff = {"X": [[2,0],[0,1]], "Y": [[1,0],[0,2]]}
11  neighbors = [[0,3],[0,4],[0,5],[1,2],[1,4],[2,3],[4,5],[5,6]]
```

```python
# Change the types of players in the game, modify each type's payoff matrix, or edit the way players communicate with each other
9   types = ["X", "X", "X", "X", "X", "X", "Y"]
10  payoff = {"X": [[5,0],[0,2]], "Y": [[2,0],[0,5]]}
11  neighbors = [[0,2],[0,4],[1,3],[1,4],[1,5],[2,3],[5,6]]
```

## Authors
Natalia Koliou & Konstantinos Chaldaiopoulos
