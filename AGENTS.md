# Repository Guidelines

## Project Structure & Module Organization

This repository currently contains project documentation only. As the Express + React application is added, keep the codebase split by runtime:

```text
client/          # React UI, components, styles, and static assets
server/          # Express app, routes, middleware, and API logic
client/src/      # Frontend source modules
server/tests/    # Backend tests
client/src/**/*.test.*  # Frontend tests, colocated where practical
```

Keep reusable UI in `client/src/components/`, page-level views in `client/src/pages/`, and API routes in `server/routes/`. Avoid mixing browser code with server code.

## Build, Test, and Development Commands

Run commands from the relevant application directory once `client/package.json` and `server/package.json` exist:

```bash
cd client && npm install && npm run dev    # Start the React development server
cd client && npm run build                 # Create a production frontend build
cd server && npm install && npm run dev    # Start Express with development reloads
cd server && npm start                     # Run Express in production mode
npm test                                   # Run the package's configured tests
```

Check each package's `package.json` before adding or changing scripts. Do not assume a tool is installed without declaring it in dependencies.

## Coding Style & Naming Conventions

Use 2-space indentation for JavaScript, JSON, and CSS. Prefer semicolons and single quotes unless the existing formatter says otherwise. Name React components in `PascalCase` (for example, `UserProfile.jsx`); use `camelCase` for functions and variables; and use descriptive kebab-case filenames only for non-component assets (for example, `user-avatar.png`).

Keep Express routes resource-focused, such as `server/routes/users.js`, and export small, testable handlers. If ESLint or Prettier is introduced, run it before committing and do not hand-format against its output.

## Testing Guidelines

Add tests with each behavior change. Use the test framework configured in the relevant package and name files `*.test.js`, `*.test.jsx`, or the convention already used there. Cover successful behavior, invalid input, and API error responses. Run the applicable `npm test` command before opening a pull request.

## Commit & Pull Request Guidelines

The existing history uses concise imperative commits: `Add project README`. Follow that style, for example `Add user login route` or `Fix profile form validation`.

Keep commits focused. Pull requests should state what changed, why, and how it was tested; link related issues when available. Include screenshots or short recordings for visible React UI changes, and note any required environment variables or migration steps.

## Security & Configuration

Store secrets in untracked `.env` files, never in client-side source code or commits. Document required variable names in `.env.example` without real values.
