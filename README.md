# Next.js 15 Client-Side Navigation Error: Uncaught ReferenceError

This repository demonstrates a runtime error in Next.js 15 that occurs during client-side navigation when a page references an undefined variable. The error is not caught during the build process, leading to a broken user experience.

## Problem

The `about.js` file attempts to use a variable (`nonExistentVariable`) that is not defined.  This causes a runtime `ReferenceError` when navigating to the `/about` route after the initial page load (client-side navigation).

## Solution

The solution in `aboutSolution.js` addresses this by adding proper error handling. The undefined variable is checked before use. If it's undefined, a default value is used. This prevents the runtime error.

## Reproduction

1. Clone this repository.
2. Run `npm install`.
3. Run `npm run dev`.
4. Navigate to `/about` after the initial load of the home page. The error will occur.

After applying the fix in the solution file, the error will no longer occur.