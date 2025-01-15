# Unnecessary re-renders in React useEffect hook

This repository demonstrates a common React bug involving unnecessary re-renders within the `useEffect` hook. The `useEffect` hook is intended for side effects, and when it is not properly used it can lead to performance issues.

## Bug
The `bug.js` file contains a component that uses `useEffect` to log the count to the console after each render.  This is inefficient because the log is triggered even when the count doesn't change, causing redundant work and potentially impacting performance.

## Solution
The `bugSolution.js` file demonstrates a correct implementation that utilizes the optional dependency array in `useEffect`. By including `count` in the dependency array, the effect only runs when the count changes. This approach makes the code more efficient and avoids unnecessary re-renders and console logs.

## How to reproduce
1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the console logs and the component's behavior.