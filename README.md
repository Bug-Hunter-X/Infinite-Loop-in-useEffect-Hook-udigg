# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook that leads to an infinite loop.  The example shows how updating state within the `useEffect` without proper dependency management can cause unexpected behavior.

## Bug Description
The bug is caused by the incorrect usage of the `useEffect` hook. The state `count` is updated inside the `useEffect`, causing a re-render, which in turn triggers the `useEffect` again, creating an infinite loop. The `useEffect` should only update state when necessary, based on changes in its dependencies. 

## Solution
The solution avoids the infinite loop by correctly managing dependencies in the `useEffect` hook. By adding `count` as a dependency, `useEffect` will only run when the value of `count` changes.
