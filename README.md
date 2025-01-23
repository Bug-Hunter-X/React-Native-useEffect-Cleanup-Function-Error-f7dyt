# React Native useEffect Cleanup Function Error

This repository demonstrates a common yet elusive bug in React Native applications involving the `useEffect` hook and its cleanup function.  The issue arises when the cleanup function attempts to access variables or objects that are no longer available because the component has unmounted.  This often results in cryptic error messages, making debugging challenging.

The `bug.js` file showcases the problematic code. The `bugSolution.js` file presents a solution to prevent the error.

## Reproducing the Bug

1. Clone this repository.
2. Run `npm install`.
3. Run the application using your preferred React Native method.
4. Observe the error console messages upon unmounting the component.

## Solution

The solution lies in checking if the component is still mounted before performing any actions within the cleanup function.  This is crucial to prevent undefined behavior and ensure the application's stability.