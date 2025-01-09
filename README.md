# React Native Uninitialized State Variable Access

This repository demonstrates a common error in React Native applications: attempting to access a state variable before it has been initialized. This usually occurs when asynchronous operations, like fetching data from an API, are involved.

## The Problem

The `bug.js` file shows a component that tries to access `data.someProperty` before the `useEffect` hook has finished fetching and setting the data.  This results in a `Cannot read properties of null (reading 'someProperty')` error.

## The Solution

The `bugSolution.js` file demonstrates how to correctly handle this. We introduce a conditional rendering to only display the data once it's available.