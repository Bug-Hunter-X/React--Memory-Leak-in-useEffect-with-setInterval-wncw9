# React Memory Leak Bug

This repository demonstrates a common bug in React applications involving memory leaks caused by the improper use of `setInterval` within the `useEffect` hook.

The `bug.js` file contains the buggy component. The `bugSolution.js` shows the corrected implementation.

## Bug Description

The original code lacks a cleanup function in the `useEffect` hook, leading to a memory leak. When the component unmounts, `setInterval` continues to run, consuming resources.

## Solution

The solution involves using the return value of `useEffect` to implement a cleanup function. This function clears the interval when the component unmounts, preventing the leak.

## How to Reproduce

1. Clone this repository.
2. Navigate to the directory containing `bug.js`.
3. Run the React application (ensure you have Node.js and npm installed).