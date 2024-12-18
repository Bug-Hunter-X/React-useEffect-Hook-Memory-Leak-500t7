# React useEffect Hook Memory Leak

This repository demonstrates a common but easily overlooked error in React: forgetting to include a cleanup function in the `useEffect` hook.  This can lead to memory leaks and unexpected behavior.

## Bug

The `bug.js` file contains a React component that uses the `useEffect` hook to log a message to the console when the component mounts. However, it's missing the crucial `return` statement that provides a cleanup function. This means that any side effects initiated within the `useEffect` will not be cleaned up when the component unmounts.

## Solution

The `bugSolution.js` file shows the corrected version.  The addition of the `return` statement and a cleanup function ensures that any cleanup tasks (in this case, simply logging a message) will be executed when the component is unmounted, preventing potential memory leaks.