# React useEffect setInterval Memory Leak

This example demonstrates a common mistake in React: using `setInterval` within a `useEffect` hook without proper cleanup. This leads to memory leaks because the interval continues running even after the component is unmounted.

## Bug
The `bug.js` file shows the faulty implementation.  The `setInterval` is started, but never stopped, resulting in a memory leak.

## Solution
The `bugSolution.js` demonstrates the correct approach.  A cleanup function is returned from the `useEffect` hook. This function clears the interval when the component unmounts, preventing the memory leak.

## How to Reproduce
1. Clone this repository.
2. Open `bug.js` and `bugSolution.js` to see the buggy and fixed code.
3. Observe the behaviour when running each component.