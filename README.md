# React SetInterval Memory Leak
This example demonstrates a common mistake when using `setInterval` within a React component's `useEffect` hook.  Forgetting to return a cleanup function leads to memory leaks as the interval continues to run even after the component unmounts.

## Bug
The `bug.js` file contains a React component that uses `setInterval` to update a counter. However, it lacks a cleanup function to stop the interval when the component unmounts, causing a memory leak.

## Solution
The `bugSolution.js` file shows the corrected component, including a return statement within the `useEffect` cleanup function to stop the `setInterval` when the component is no longer needed.