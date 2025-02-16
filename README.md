# React Native Asynchronous State Update Race Condition

This repository demonstrates a common race condition bug in React Native applications where asynchronous data fetching and state updates lead to inconsistent UI behavior. The bug occurs when multiple asynchronous operations modify the component's state concurrently, resulting in unexpected or outdated UI updates.

## Problem
The `bug.js` file contains a component that fetches data and updates its state. Due to the asynchronous nature of data fetching, there's a possibility of a race condition where another action modifies the state before the data fetch completes. This leads to the UI not accurately reflecting the latest data.

## Solution
The `bugSolution.js` file presents a solution that utilizes the `useEffect` hook and the `Promise.all` method to ensure all asynchronous operations complete before updating the state. This approach prevents race conditions by synchronizing state updates.