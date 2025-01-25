# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React applications where an infinite loop is created due to improper usage of the `useEffect` hook. The `useEffect` hook is designed to perform side effects after rendering, but if it modifies state in a way that triggers another render, an infinite loop can result.

## Bug Description

The `bug.js` file contains a component that uses the `useEffect` hook to increment a counter. The dependency array is missing `count`, causing the effect to run after every render, and constantly updating the count. This leads to an infinite render loop.

## Solution

The `bugSolution.js` file provides a corrected version of the component that fixes the issue. The dependency array now correctly includes `count`, ensuring that the effect only runs when `count` changes. This prevents the infinite loop.

## How to reproduce the bug

1. Clone this repository
2. Run `npm install`
3. Run `npm start`
4. Observe the infinite loop in the browser console or the browser crashing.

## How to fix the bug

1. Clone this repository
2. Run `npm install`
3. Replace `bug.js` with `bugSolution.js`
4. Run `npm start`
5. Observe that the counter updates correctly and no longer causes an infinite loop.