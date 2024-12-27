# React UseEffect Infinite Loop Bug

This repository demonstrates a common React bug: an infinite loop caused by incorrectly updating state within a useEffect's callback.

## Description
The bug occurs in `bug.js`.  The `useEffect` hook attempts to update the `count` state within its own callback. This creates a continuous cycle of updates, leading to an infinite loop and a crashed application.

## Solution
The solution, found in `bugSolution.js`, uses the functional update approach to avoid this issue. The `setCount` function receives the previous state as an argument, ensuring a proper update without causing an infinite loop.