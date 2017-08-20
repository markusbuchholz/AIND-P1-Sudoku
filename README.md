# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A: In order to solve the naked twins problem the  strategy with following steps was applied:
1. For incoming to the function dictionary – values, the key for each box (for each unit) with the value equals 2 is collected (twin_keys).
2.	In addition it is created twin_value list which holds the values of “keys” 
3.	The list twins_m is created.
3.	For each of 27 units (in unitlist) and before selected keys the comparision of two box value is performed – in order to check if two the same values exist in common unit.
4. If two the same value exist so the key of these values are added to common twins_m list (created in step. 3).
5. Finally, successful detection of twins makes possible to check if among other boxes (in unit) exist the same digit of number (one by one). If the same digit (like twin has) exists so this digit is removed from box value/number.   


# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A: In order to solve ordinary sudoku problem the constrain propagation is used. The “eliminate”, “only_choice” and finally “naked_twin” strategies are applied for the row, column and square units. In order to find solution for diagonal sudoku mentioned strategies have to be applied also for two more units: diagonals of the sudoku. These diagonal constraints are automatic created and incorporated into unitlist. 

### Install

This project requires **Python 3**.

We recommend students install [Anaconda](https://www.continuum.io/downloads), a pre-packaged Python distribution that contains all of the necessary libraries and software for this project. 
Please try using the environment we provided in the Anaconda lesson of the Nanodegree.

##### Optional: Pygame

Optionally, you can also install pygame if you want to see your visualization. If you've followed our instructions for setting up our conda environment, you should be all set.

If not, please see how to download pygame [here](http://www.pygame.org/download.shtml).

### Code

* `solution.py` - You'll fill this in as part of your solution.
* `solution_test.py` - Do not modify this. You can test your solution by running `python solution_test.py`.
* `PySudoku.py` - Do not modify this. This is code for visualizing your solution.
* `visualize.py` - Do not modify this. This is code for visualizing your solution.

### Visualizing

To visualize your solution, please only assign values to the values_dict using the ```assign_values``` function provided in solution.py

### Submission
Before submitting your solution to a reviewer, you are required to submit your project to Udacity's Project Assistant, which will provide some initial feedback.  

The setup is simple.  If you have not installed the client tool already, then you may do so with the command `pip install udacity-pa`.  

To submit your code to the project assistant, run `udacity submit` from within the top-level directory of this project.  You will be prompted for a username and password.  If you login using google or facebook, visit [this link](https://project-assistant.udacity.com/auth_tokens/jwt_login for alternate login instructions.

This process will create a zipfile in your top-level directory named sudoku-<id>.zip.  This is the file that you should submit to the Udacity reviews system.



