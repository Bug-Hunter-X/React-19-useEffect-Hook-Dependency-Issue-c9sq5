# React 19 useEffect Hook Dependency Issue

This repository demonstrates a common error encountered when using the `useEffect` hook in React 19: forgetting to include state variables in the dependency array, leading to unexpected behavior and potential bugs.

## Bug Description

The `bug.js` file contains a component that uses `useState` to manage a counter. The `useEffect` hook logs the current count to the console after each render.  However, the `count` variable is missing from the dependency array, causing the effect to run only once instead of after every update of `count`, resulting in an incorrect log.

## Solution

The `bugSolution.js` file shows the corrected version where `count` is added to the dependency array, ensuring the effect runs whenever the count changes, resolving the bug.  This is crucial for keeping the component's behavior consistent with the state changes.