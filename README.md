# React UseEffect Cleanup

This repository demonstrates a common mistake when using the `useEffect` hook in React: forgetting to include a cleanup function to prevent memory leaks.

The `bug.js` file contains a component that uses `setInterval` inside a `useEffect` hook without a cleanup function.  This will continue to increment a counter even after the component is unmounted, leading to a memory leak.

The `bugSolution.js` file shows the corrected version with the cleanup function that uses `clearInterval` to stop the interval when the component is unmounted.