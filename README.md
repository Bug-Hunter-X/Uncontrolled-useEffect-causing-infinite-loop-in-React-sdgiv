# Uncontrolled useEffect causing infinite loop in React

This repository demonstrates a common React bug involving the `useEffect` hook.  The provided code shows an `useEffect` hook without a dependency array, leading to an infinite loop.  The solution demonstrates how to fix this by adding the correct dependencies to the `useEffect` hook.

## Bug
The `useEffect` hook in `bug.js` is called after every render because it lacks a dependency array.  This results in an infinite loop, causing excessive re-renders and console output, potentially impacting application performance.

## Solution
The solution in `bugSolution.js` adds `[count]` as the dependency array to `useEffect`. This ensures that the effect runs only when the `count` value changes, preventing the infinite loop.

## How to reproduce the bug
1. Clone this repo.
2. Run `npm install`
3. Run `npm start` (or your preferred React development server)
4. Observe the infinite loop in your browser's console and the performance degradation.

## How to fix the bug
Review the solution in `bugSolution.js` to see the corrected `useEffect` implementation.  The key is to add the state variable (or any other variables that affect the effect's behaviour) to the dependency array.