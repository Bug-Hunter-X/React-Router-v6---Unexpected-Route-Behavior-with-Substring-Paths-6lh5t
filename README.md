# React Router v6 - Unexpected Route Behavior with Substring Paths

This repository demonstrates a subtle bug in React Router v6 when dealing with routes where one path is a substring of another.  The longer route always seems to take precedence, regardless of the order in which they are defined in the `Routes` component.

The issue is evident in `bug.js`. The `/contact` route should be rendered when navigating to `/contact`, but instead, the `/about` route is always rendered. This is because `/contact` is a substring of `/contact-us`.

The solution, provided in `bugSolution.js`, demonstrates using the `path` attribute in Route correctly to only render it for the exact path.