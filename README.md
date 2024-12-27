# React useEffect Hook Missing Dependency
This example demonstrates a common error in React's `useEffect` hook: omitting necessary dependencies from the dependency array.  This leads to unexpected behavior where the effect doesn't run when expected, resulting in stale closures and potential bugs.

## Problem
The provided code uses `useEffect` to log a message to the console whenever the component renders. However, the dependency array is empty (`[]`), meaning the effect only runs once after the initial render.  Subsequent changes to the `count` state variable don't trigger the effect to re-run, causing the console log to show only once, even when the count changes.

## Solution
To fix this issue, we must include `count` in the dependency array. This ensures the effect runs whenever the `count` value changes, resulting in the expected console log output on every increment of the counter.
