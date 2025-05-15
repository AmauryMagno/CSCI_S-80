#Search Algorithm

## Pass to find a goal
- Agent
- State
- Transition Model
- State Space
- Goal Path: The condition that determines whether a given state is a goal state. For example, in a navigator app, the goal test would be whether the current location of the agent (the representation of the car) is at the destination. If it is — problem solved. If it’s not — we continue searching.
- Path Cost: A numerical cost associated with a given path. For example, a navigator app does not simply bring you to your goal; it does so while minimizing the path cost, finding the fastest way possible for you to get to your goal state.

## Solving Search Problems
### Data is stored in a **node**, it contains:
- A state
- Its parent node, through which the current node was generated
- The action that was applied to the state of the parent to get to the current node
- The path cost from the initial state to this node

### You need use frontier, a mechanism that "manage" the nodes:
Repeat:
1. If the frontier is empty,
   
    * Stop. There is no solution to the problem.
   
3. Remove a node from the frontier. This is the node that will be considered.

4. If the node contains the goal state,  
    * Return the solution. Stop.

    Else,  
    * Expand the node (find all the new nodes that could be reached from this node), and add resulting nodes to the frontier.
    * Add the current node to the explored set.
