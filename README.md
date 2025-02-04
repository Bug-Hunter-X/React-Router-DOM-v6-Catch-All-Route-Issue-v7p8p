# React Router DOM v6 Catch-All Route Issue

This repository demonstrates a common issue encountered when using the catch-all route ("*" route) in React Router DOM v6.  The problem arises when the catch-all route doesn't correctly handle navigation to non-existent paths, resulting in unexpected behavior or no rendering at all.

## Problem Description
The provided `App.js` contains three routes: "/", "/about", and a catch-all route "*".  Despite the catch-all route being defined, it does not render the `NotFound` component when navigating to an invalid route.  Instead, it may render nothing or the previous component.

## Solution
The solution involves ensuring the catch-all route is placed at the end of the route definitions within the `Routes` component.  This ensures that it acts as a true fallback route, only matching if no other routes match the URL.
