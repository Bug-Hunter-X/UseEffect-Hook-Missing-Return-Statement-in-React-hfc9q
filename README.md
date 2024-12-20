# React useEffect Hook Missing Return Statement

This repository demonstrates a common error in React applications: forgetting to include a return statement in the `useEffect` hook.  This can lead to memory leaks and unexpected behavior.  The example shows how to fix the issue by properly cleaning up the effect.

## Bug Description

The provided code snippet uses `useEffect` to update the document title whenever the `count` state variable changes. However, it is missing a `return` statement within the `useEffect` callback. This omission prevents the cleanup function from being called, potentially leading to memory leaks, especially if the component unmounts before the effect's logic is completed.

## Bug Solution

The solution involves adding a return statement to the `useEffect` callback, which provides a cleanup function.  This function is called before the component unmounts or before the next effect execution.  This ensures any resources or event listeners are properly released, preventing memory leaks.