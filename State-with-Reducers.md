# Advanced State-with-Reducers

## useReducer

```
const [state, dispatch] = useReducer(reducer, initialArg, init);
```

An alternative to useState. Accepts a reducer of type (state, action) => newState, and returns the current state paired with a dispatch method. (If you’re familiar with Redux, you already know how this works.)

useReducer is usually preferable to useState when you have complex state logic that involves multiple sub-values or when the next state depends on the previous one. useReducer also lets you optimize performance for components that trigger deep updates because you can pass dispatch down instead of callbacks.

### Specifying the initial state

There are two different ways to initialize useReducer state. You may choose either one depending on the use case. The simplest way is to pass the initial state as a second argument:

```
  const [state, dispatch] = useReducer(
    reducer,
    {count: initialCount}
  );
```

Note

React doesn’t use the state = initialState argument convention popularized by Redux. The initial value sometimes needs to depend on props and so is specified from the Hook call instead. If you feel strongly about this, you can call useReducer(reducer, undefined, reducer) to emulate the Redux behavior, but it’s not encouraged.

## Ultimate Guide to useReducer

useReducer is one of the additional Hooks that shipped with React v16.8. An alternative to the useState Hook, useReducer helps you manage complex state logic in React applications. When combined with other Hooks like useContext, useReducer can be a good alternative to Redux, Recoil or MobX. In certain cases, it is an outright better option.

### How does the useReducer Hook work?

The useReducer Hook is used to store and update states, just like the useState Hook. It accepts a reducer function as its first parameter and the initial state as the second.

useReducer returns an array that holds the current state value and a dispatch function to which you can pass an action and later invoke it. While this is similar to the pattern Redux uses, there are a few differences.

For example, the useReducer function is tightly coupled to a specific reducer. We dispatch action objects to that reducer only, whereas in Redux, the dispatch function sends the action object to the store. At the time of dispatch, the components don’t need to know which reducer will process the action.

### The dispatch method

The dispatch function accepts an object that represents the type of action we want to execute when it is called. Basically, it sends the type of action to the reducer function to perform its job, which, of course, is updating the state.

The action to be executed is specified in our reducer function, which in turn, is passed to the useReducer. The reducer function will then return the updated .
