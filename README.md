# Incorrect useEffect Dependency Array in React
This example demonstrates a common bug in React's `useEffect` hook where the dependency array is missing a necessary state variable, leading to an infinite loop.  The `setInterval` function continues to update the state without ever letting the component settle, causing a continuous re-render cycle.

## Bug
The `bug.js` file contains the buggy code.  The `useEffect` hook attempts to update the `count` state every second using `setInterval`. However, the dependency array `[]` is empty, meaning that the effect runs only once after the initial render. Because the component re-renders continuously, the effect will run again and again, creating a loop. 