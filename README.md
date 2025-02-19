# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving the `useEffect` hook. The component renders infinitely, causing excessive console logging and potential performance issues.

## Bug Description

The provided `MyComponent` utilizes `useEffect` without a dependency array.  This means the effect runs after every render, leading to an infinite loop because updating `count` triggers a re-render, which triggers the effect again, and so on. 

## Solution

The solution involves adding a dependency array to the `useEffect` hook, specifying that the effect should only run when `count` changes.
