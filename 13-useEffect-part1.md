# useEffect - Introduction

This hook renders and emulates the side-effects in a react application. In react, side-effects means any script or component that is present outside the current component or may even be present at the top level.

Ex. Signup, fetching data, adding event-listeners, etc.

useEffect can work within a callback function as well.

By default, useEffect, runs after every render, re-render, or a component change. However we can change this behaviour.

There can be multiple useEffect calls in a single component.

## Cleanup function

The useEffect hook has a second parameter which is an array also known as the list of dependancies or the dependancy array. It instructs the DOM to trigger the useEffect only when there is a change in the variables that have been passed in the dependancy array.

## 2nd parameter

The useEffect also has a cleanup function which reverst the action applied by the useEffect and restores the original state of the component or the entire App. Each and every useEffect call must have a cleanup function so that each and every action is reverted to its original state and there are no memory leaks, makking the app incredibly faster.
