# Repeated Coordination Game

* The code implements a Repeated Coordination Game between 7 players using Q-Learning.
* The game involves two actions, "Action[1]" and "Action[2]", and two types of players, "X" and "Y".
* The payoffs for each player depend on the combination of actions chosen by the player and the pairs in which he is involved in a given round.
* The neighbors list specifies the pairs of players that are matched together in each round, and each player may participate in multiple pairs depending on the size and structure of the network.
* The game is played over a series of episodes, and the players' Q-tables are updated according to the rewards received during the moments of each episode.
* The exploration rate gradually decreases over the course of the game in order to encourage players to exploit the game more often as the game progresses.
* The performance of the players is graphed over time, and the final Q-tables for each player are printed at the end of the game.


#### Functions of the code ####
* The "qlearning" function is the main function that orchestrates the game, calling the other functions as needed.
* During the game, the "game_print" function is responsible for printing the state of the game during each round of exploration and exploitation.
* The "graph" function is used generates graphs that show how the player choses actions and recieves his rewards evolve over time.
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
This code provides a basic implementation of an ML Ciphertext Decryption Algorithm. Users are encouraged to modify the training/testing datasets or the feature-tuple, to observe the impact on the total performance and accuracy.

Here are some suggestions:
```python
# Remove some good features from the feature tuple:
117  fig, axs = plt.subplots(nrows=3, ncols=3, figsize=(12, 8))
...
120  for d in (f0, f1, f2, f3, f4, f8, f9, f10, f11):
```

```python
# Use a different testing dataset:
87   training_text = "TRAINING-tolstoy-anna-karenina.txt"
88   testing_text = "TESTING-goethe-werther.txt"
89   decryption_alphabet = "ghbcafmsztwnroevlixupjyqkd"  # encryption_alphabet = "ecdzofabrvyqglnuxmhjtpkswi"
```

## Authors
Natalia Koliou & Konstantinos Chaldaiopoulos
