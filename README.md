# React Router v6 Catch-all Route Issue

This repository demonstrates a common issue encountered when using the catch-all route (`/*`) in React Router v6. The catch-all route, meant to handle 404 errors, unexpectedly interferes with other routes, overriding their intended behavior.

The problem arises from the order and placement of routes.  The catch-all route, if placed before other specific routes, will always match, regardless of the URL.

**How to reproduce:**
1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Navigate to `/about` - the route will not render correctly.

**Solution:**
The solution involves carefully ordering routes. The catch-all route should always be placed last to ensure it only matches when no other routes are matched.  The `AppSolution.js` file provides the corrected code.