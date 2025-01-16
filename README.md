# React 19 useEffect Bug: Unnecessary Re-renders

This repository demonstrates a common React 19 issue where the `useEffect` hook runs after every render, even when it doesn't need to.  This can lead to performance problems, especially in complex components.

## Bug Description

The provided `bug.jsx` file contains a simple counter component. The `useEffect` hook logs a message to the console after each render.  This is inefficient because the effect doesn't depend on any values that change between renders.   React 19's strict mode doesn't automatically catch it, requiring developers to focus on the dependency array.

## Solution

The `bugSolution.jsx` file shows the corrected code. By adding an empty dependency array `[]` to the `useEffect` hook, we ensure it only runs once after the initial render.