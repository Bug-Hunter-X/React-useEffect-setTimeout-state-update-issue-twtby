# React useEffect setTimeout State Update Issue

This repository demonstrates a common issue encountered when using the `useEffect` hook in React with `setTimeout` to update state.  The provided code intends to increment a counter every second, but due to a closure issue, it only increments once.

## Problem
The `setTimeout` callback function within `useEffect` captures the initial value of `count` (0) due to closure.  Thus, it always adds 1 to 0, resulting in the count staying at 1.

## Solution
The solution involves using a functional update to `setCount` to ensure the latest value is used.