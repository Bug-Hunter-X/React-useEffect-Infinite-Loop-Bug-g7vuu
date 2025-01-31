# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving the `useEffect` hook, specifically an infinite loop caused by incorrect dependency management and flawed logic. 

## Bug Description
The `MyComponent` component uses `useEffect` to reset the count when it exceeds 5. However, the dependency array is missing `someExternalState`, leading to an infinite loop when `someExternalState` changes.  Additionally, setting `count` to 0 inside the effect leads to an immediate re-render and triggers the effect again.

## Solution
The solution addresses both the missing dependency and the incorrect logic, ensuring that the `useEffect` hook runs only when necessary. 

## How to reproduce
1. Clone this repository.
2. Run `npm install`
3. Run `npm start`
4. Observe the counter's behavior and console logs.