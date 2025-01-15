# Infinite useEffect Loop in React

This repository demonstrates a common React bug: an infinite loop caused by an incorrectly used `useEffect` hook.  The `useEffect` hook, while powerful, can lead to performance issues and unexpected behavior if not used correctly.  This example highlights the importance of specifying the dependency array correctly.

## Bug Description

The initial code has an `useEffect` hook that attempts to log the current value of the `count` state variable. However, because the dependency array is missing or incorrect, the effect runs after every render, leading to an infinite loop.  The console will rapidly fill with log messages, and the application may become unresponsive.

## Solution

The solution involves properly defining the dependency array for the `useEffect` hook. By including `[count]` in the dependency array, the effect will only re-run whenever the `count` variable changes.