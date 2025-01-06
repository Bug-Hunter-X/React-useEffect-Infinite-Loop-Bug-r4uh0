# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React applications involving the `useEffect` hook.  The problem arises when the `useEffect` hook is used without specifying a dependency array. This causes the effect to run after every render, leading to an infinite loop, as changes made in the effect trigger re-renders, which in turn trigger the effect again.

The `bug.js` file contains the buggy code, while `bugSolution.js` provides the corrected version.

## How to reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server. 
4. Observe the rapidly increasing count in the console and the performance issues.

## Solution

The solution involves adding an empty dependency array `[]` to the `useEffect` hook. This ensures the effect runs only once after the initial render.