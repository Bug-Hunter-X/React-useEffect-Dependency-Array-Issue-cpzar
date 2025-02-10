# React useEffect Dependency Array Issue

This repository demonstrates a common issue with the React `useEffect` hook where the dependency array is incorrectly specified, leading to unexpected re-renders and potential performance problems.

## Problem

The `useEffect` hook is used to perform side effects after a component renders.  However, if the dependency array is missing or incorrect, the effect may run at unintended times.

In the example `bug.js`, the `useEffect` hook logs a message on every render.  This is inefficient and can lead to performance problems.

## Solution

The solution `bugSolution.js` correctly specifies `count` in the dependency array.  Now the effect only runs when the `count` value changes, significantly improving performance.

## How to reproduce

1. Clone this repo.
2. Run `npm install`.
3. Run `npm start`.
4. Observe the console logs in `bug.js` and compare to the behavior in `bugSolution.js`.