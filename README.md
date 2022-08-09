# Repro for bug with MSW, NextJS and Auth0

This repro is related to this issue: https://github.com/mswjs/msw/issues/700.

## Procedure

This project was setup using `npx create-next-app --example auth0 .`.

You need an Auth0 account to test this repro. You can follow the steps here to set it up: https://github.com/vercel/next.js/tree/canary/examples/auth0. **Only exception is that this repro expects the auth path to lives under /api/auth/ and not /api/ as shown in the link**. You'll need to configure your Auth0 App accordingly.

This repo has two tags:

- `working`
- `not-working`

You can navigate to both and run `npm run dev` to notice when it works and when it doesn't. If you try to click the "Login" button it should loads indefinitely on the latter while it does redirect you to Auth0 login page on the former.
