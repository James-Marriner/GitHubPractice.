Pig Game - James Marriner - README

All Code was run in Python version 3.13.10.

Packages used and corresponding versions are:
 - matplotlib 3.10.8
 - pymonad 2.4.0
The following are the same as the python version.
 - random 3.13.10
 - itertools 3.13.10
 - functools 3.13.10

Key Functions to Understand.

Competition = lambda Strategies,n_plays,Draw,Target, DiceRange,n_dice : ...

Strategies should be a dictionary of the strategy function ready to accept the inputs "Target" and "DiceFunc" mapping to a chosen name.
E.g. Strategies = {Roll_n_times(1) : "Roll Once"}
- The arguments of Roll_n_times are (n,Target,DiceFunc,CurrentScores)
- These should be the only arguments for any strategy used in competition

n_plays should be an integer describing the number of times each match is repeated.

Draw should be True or False depending on whether draws are allowed.

Target should be an integer for the winning score of the game

DiceRange should be a tuple inclusive for the range of a dice. e.g. a standard 6-sided die is (1,6).

n_dice should be an integer for the number of dice rolled at each roll.


Full_process =  lambda Strategies,n_plays,Draw,Target,Results : ...

The first three arguments are as described previously. 
Results should be a direct result of the Competition function specified above.


None of the created strategies have been tested at fringe cases or fitted with errors for improper inputs. This means that for example, Strategies should always contain more than one strategy. Other than this, I hope everything works and my implementation is at least at some point, interesting :)