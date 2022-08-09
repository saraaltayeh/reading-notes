# useState() Hook

## Introducing Hooks

### What was the motivation for introducing Hooks?

Hooks solve a wide variety of seemingly unconnected problems in React that we’ve encountered over five years of writing and maintaining tens of thousands of components. Whether you’re learning React, use it daily, or even prefer a different library with a similar component model, you might recognize some of these problems.

### Complex components become hard to understand

We’ve often had to maintain components that started out simple but grew into an unmanageable mess of stateful logic and side effects. Each lifecycle method often contains a mix of unrelated logic. For example, components might perform some data fetching in componentDidMount and componentDidUpdate. However, the same componentDidMount method might also contain some unrelated logic that sets up event listeners, with cleanup performed in componentWillUnmount

### Hooks allow you to reuse stateful logic without changing

Completely opt-in: You can try Hooks in a few components without rewriting any existing code.

## hooks api

### ✌️ Rules of Hooks

Only call Hooks at the top level. Don’t call Hooks inside loops, conditions, or nested functions.
Only call Hooks from React function components. Don’t call Hooks from regular JavaScript functions. (There is just one other valid place to call Hooks — your own custom Hooks. We’ll learn about them in a moment.)

### 💡 Building Your Own Hooks

Sometimes, we want to reuse some stateful logic between components. Traditionally, there were two popular solutions to this problem: higher-order components and render props. Custom Hooks let you do this, but without adding more components to your tree.

Custom Hooks are more of a convention than a feature. If a function’s name starts with ”use” and it calls other Hooks, we say it is a custom Hook. The useSomething naming convention is how our linter plugin is able to find bugs in the code using Hooks.

## the state hook

1. What is a Hook?
 A Hook is a special function that lets you “hook into” React features. For example, useState is a Hook that lets you add React state to function components. We’ll learn other Hooks later.

2. When would I use a Hook?
 If you write a function component and realize you need to add some state to it, previously you had to convert it to a class. Now you can use a Hook inside the existing function component.

3. What does calling useState do?
 It declares a “state variable”. Our variable is called count but we could call it anything else, like banana. This is a way to “preserve” some values between the function calls — useState is a new way to use the exact same capabilities that this.state provides in a class. Normally, variables “disappear” when the function exits but state variables are preserved by React.

4. What do we pass to useState as an argument?
 The only argument to the useState() Hook is the initial state. Unlike with classes, the state doesn’t have to be an object. We can keep a number or a string if that’s all we need. In our example, we just want a number for how many times the user clicked, so pass 0 as initial state for our variable. (If we wanted to store two different values in state, we would call useState() twice.)

5. What does useState return?
 It returns a pair of values: the current state and a function that updates it. This is why we write const [count, setCount] = useState(). This is similar to this.state.count and this.setState in a class, except you get them in a pair.

```
import React, { useState } from 'react';

function Example() {
  // Declare a new state variable, which we'll call "count"
  const [count, setCount] = useState(0);
```
