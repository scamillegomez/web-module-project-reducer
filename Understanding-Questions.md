# Understanding Questions:
1. What are the steps of execution from the pressing of the 1 button to the rendering of our updated value? List what part of the code excutes for each step.
* The user presses the 1 button.
* the onClick method passes down as props to the CalcButton component, and dispatches the addOne action 
* Since the action is pre-built to return a reducer properties object with type: ADD_ONE (n the actions\index file), the dispatch is actually dispatching that object  
* The TYPE property of ADD_ONE then gets applied to a case statement in the reducers\index file. The program searches for a case of type: ADD_ONE, then executes the state change specified in the return statement
*  since we passed state back to App.js, and the TotalDisplay is showing the "total" item from state, the total updates to show the previous value plus 1
