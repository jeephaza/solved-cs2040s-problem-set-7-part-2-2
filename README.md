Download Link: https://assignmentchef.com/product/solved-cs2040s-problem-set-7-part-2-2
<br>
<h2>Problem 7.d.             Maze Exploration for Real SuperPeople</h2>

In this part, as in the previous part, your job is to determine the shortest path from a specified source to a specified destination. However, you are also given the ability to bypass (demolish, jump over, or magically traverse) up to a limited number of walls along the way. Of course, you will not be allowed to use your power to demolish the outer walls that surround your maze. You begin with a fixed amount of superpowers, and every time you demolish a wall, your power reduces by one. Your goal is to find the shortest path from the start to the end.

Create a new class MazeSolverWithPower that implements IMazeSolverWithPower which contains the overridden method:

Integer pathSearch(int startRow, int startCol, int endRow, int endCol, int superpowers).

It should return an integer representing the minimum number of steps needed if a path is found, or null if no such path is available. As before, it should also update, for each room, the onPath attribute. (Notice that the IMazeSolverWithPower interface inherits from IMazeSolver, and hence must correctly implement all the methods from there as well. In this case, if numReachable is called after a pathSearch with superpowers, then its answer should also be based on having the same number of superpowers (in addition to having the same starting location))

<em>Hint: </em>One strategy is to represent the state as a combination of the current room and the remaining amount of superpower. If you explore this graph of all possible states, you will visit all possible rooms, with all possible remaining amounts of superpower.