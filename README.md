# React setInterval Memory Leak

This repository demonstrates a common memory leak in React applications caused by improper use of `setInterval` within a component's `useEffect` hook.  The example shows how to fix this issue by including a cleanup function in the `useEffect` hook to clear the interval before the component unmounts.

## Problem
The provided `MyComponent` uses `setInterval` to update a counter every second.  However, it omits the crucial cleanup function required in `useEffect` to stop the interval when the component unmounts.  This leads to a memory leak, as the interval continues running even after the component is removed from the DOM.

## Solution
The solution demonstrates the correct usage of `useEffect` with `setInterval`.  It includes a cleanup function that uses `clearInterval` to stop the interval when the component unmounts, preventing the memory leak.

## How to run
Clone this repository and run `npm install` to install the necessary dependencies.
Then, you can run the project using `npm start`.
