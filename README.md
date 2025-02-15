# React Router Dom v6 Catch All Route Issue

This repository demonstrates a common issue encountered when using catch-all routes (`/*`) in React Router Dom v6.  The catch-all route is unexpectedly matching even when other routes should take precedence.

## Problem
The provided example shows a simple app with routes for `/` and `/about`. The `/*` route is intended to handle 404 scenarios. However, regardless of the URL, the `NotFound` component is always rendered.

## Solution
The issue is resolved by ensuring the catch-all route is placed last in the `Routes` component. React Router matches routes in order, so the `/*` route would always be matched first. By reordering it, other more specific routes are correctly matched before the catch-all.