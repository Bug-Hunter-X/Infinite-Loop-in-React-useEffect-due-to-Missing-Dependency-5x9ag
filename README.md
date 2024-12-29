# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook: an infinite loop caused by a missing dependency in the dependency array.  The `useEffect` hook, without a properly specified dependency array, will run after every render, potentially triggering an infinite loop if it modifies state which causes a re-render.

## Bug Description:
The `bug.js` file contains a React component with a `useEffect` hook that lacks the correct dependency.  This leads to the component continuously re-rendering, resulting in an infinite loop and console spam. 

## Solution:
The `bugSolution.js` file demonstrates the correct way to use `useEffect` by adding the correct dependency in the dependency array. This ensures that the effect only runs when the count changes. 

## How to reproduce:
1. Clone the repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe the infinite loop (console spam) in the browser's developer console for `bug.js`.
5. Switch to `bugSolution.js` to see the correct behavior.