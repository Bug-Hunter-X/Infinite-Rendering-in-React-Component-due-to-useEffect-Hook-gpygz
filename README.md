# Infinite Rendering Bug in React

This repository demonstrates a common React bug involving the `useEffect` hook, which causes infinite re-rendering.

## Problem
The `useEffect` hook in the provided component lacks a dependency array. As a result, it runs after every render, causing a continuous loop of updates, and eventually leads to performance issues or browser crashes. 

## Solution
To fix the issue, add a dependency array to the `useEffect` hook to control when it runs. If you want the effect to run only once after the initial render, pass an empty array `[]` as the dependency array. Otherwise, list the state variables that cause changes requiring reruns of the effect. 