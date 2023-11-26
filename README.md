# ai_search_Haward
### This is about the search problem from CS50. url: **[link](https://video.cs50.io/WbzNRTTrX0g?screen=0Towr-pBuzw&start=321)**
![image name](https://github.com/shiqianokamiai/ai_search_Haward/assets/151977259/01e3364c-b9d3-4481-884e-f94f4b752d0d)
~~~
print('hello world')
~~~
(just wanna try to use the functions in stackedit. It is pretty cool actually.)

### Firstly, some basic concepts are to be defined in my comprehension.
1. Agent: entity that perceives its environment and acts upon those environments, like♟️, puzzles, or other competitive games. 
 2. State: a configuration of the agent and its environment, when playing tic tac toe, we have several choices to put our sign in the 9x9 squares after opponents' actions.
 3.  Initial state: the first configuration.
2. Actions: choices that can be done in a state.
![IMG_5070](https://github.com/shiqianokamiai/ai_search_Haward/assets/151977259/ca1742c2-2365-4c38-8b50-d017c1a1a145)
4.  ACTION(S): set of actions that can be executed in state S. The bracketed S is the number of the state.

##### I will try to use my paper and pen to describe these concepts vividly.
##### :+1::+1::+1::+1::+1:(funny emoji)


6. Transition model: a description of what state results from performing any available action in any state.
	![IMG_5071](https://github.com/shiqianokamiai/ai_search_Haward/assets/151977259/b78ed952-fdc9-44fa-99b5-73b1c071f5e3)
	RESULT(s, a) returns the state resulting from performing action a in state s.
	
7. State space: the set of all states reachable from the initial state by any sequence of actions.

![IMG_5072](https://github.com/shiqianokamiai/ai_search_Haward/assets/151977259/7894bf27-febf-47aa-8d98-93c688102153)

9. Goal test: way to determine whether a given state is a goal state. 
10. Path cost: numerical cost associated with a given path.
11.  Solution: a sequence of actions that leads from the initial state to a goal state.
12. Optimal solution: the solution that has the lowest path cost.
13.  Node: a data structure that keeps track of (different features)
     - a state
     - a parent (node that generated this node)
     - an action (action applied to parent to get node)
     - a path cost (from initial state to node) 
   
Approach
- 
- Start with a  frontier that contains the initial state:
- Repeat:
		 1. if the frontier is empty, then no solution
		 2. remove a node from the frontier
		 3. if node contains goal state, return the solution
		 4. expand node, add resulting nodes to the frontier
		![IMG_5073](https://github.com/shiqianokamiai/ai_search_Haward/assets/151977259/e0d1dc3f-a8a1-4538-97e2-d8155b70adea)
		
		
Revised Approach
-
- Start with a frontier that contains the initial state.
- Start with an empty **explored set**.
- If node contains **goal state**, return the solution,
- Add the node to the explored set.
- **Expand node**, add resulting nodes to the frontier if they aren't already in the frontier or the explored set.
- 
