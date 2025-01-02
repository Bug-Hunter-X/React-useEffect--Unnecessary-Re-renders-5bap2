# React useEffect: Unnecessary Re-renders
This repository demonstrates a common React performance issue caused by the improper use of the `useEffect` hook. The `useEffect` hook, without the proper dependency array, will run on every render, leading to unnecessary calculations and potential performance bottlenecks.  This example showcases the problem and provides a corrected version.

## Problem
The initial `bug.js` file contains a `useEffect` hook that runs on every render because the dependency array is missing or incomplete. This causes the `console.log` statement to execute more often than necessary, impacting performance in more complex applications.

## Solution
The `bugSolution.js` file demonstrates the correct usage of the `useEffect` hook. By specifying the `count` variable in the dependency array (`[count]`), the effect only runs whenever the `count` state changes, significantly improving performance.