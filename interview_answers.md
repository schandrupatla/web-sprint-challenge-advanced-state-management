# Interview Answers
Be prepared to demonstrate your understanding of this week's concepts by answering questions on the following topics. These will not be counted as a part of your sprint score but will be helpful for preparing you for your endorsement interview, and enhancing overall understanding.

1. What problem does the context API help solve?
-The Context API was created to solve a specific problem in react, sharing state down a component tree. Similar to the solution that Redux and React-Redux libraries solve, this solution prevents prop drilling

2. In your own words, describe `actions`, `reducers` and the `store` and their role in Redux. What does each piece do? Why is the store known as a 'single source of truth' in a redux application?
-*Actions:
-An action, is an object that contains the payload of information. They are the only source of information for the Redux store to be updated. Reducers update store based on the value of the action
-Actions are the only source of information for the store as per Redux official documentation. It carries a payload of information from your application to store. As discussed earlier, actions are plain JavaScript object that must have a type attribute to indicate the type of action performed.
*Reducer:
-A reducer is a function that determines changes to an application's state. It uses the action it receives to determine this change. ... Redux relies heavily on reducer functions that take the previous state and an action in order to execute the next state
*Reducer Rules:
-They should only calculate the new state value based on the state and action arguments
They are not allowed to modify the existing state. Instead, they must make immutable updates, by copying the existing state and making changes to the copied values.
They must not do any asynchronous logic or other "side effects"
*Store:
-A store is an immutable object tree in Redux. A store is a state container which holds the application's state. Redux can have only a single store in your application. Whenever a store is created in Redux, you need to specify the reducer

3. What does `redux-thunk` allow us to do? How does it change our `action-creators`?
-Redux Thunk middleware allows you to write action creators that return a function instead of an action. The thunk can be used to delay the dispatch of an action, or to dispatch only if a certain condition is met. The inner function receives the store methods dispatch and getState as parameters.

4. What is your favorite state management system you've learned and this sprint? Please explain why!
-Redux is a predictable state container designed to help you write JavaScript apps that behave consistently across client, server, and native environments and are easy to test. While it's mostly used as a state management tool with React, we can use it with any other JavaScript framework or library
-it provides a central store that holds all states of our application. Each component can access the stored state without sending it from one component to another. Here is a simple view of how Redux works. There are three building parts: actions, store, and reducers.
-Though its very hard and confusing to use Redux, its has its own pros:
It is very difficult to reuse the components in React because it is tightly coupled with the root component. Redux reduces this complexity and provides global accessibility that helps to build applications that work frequently; are easy to test and run in different environments