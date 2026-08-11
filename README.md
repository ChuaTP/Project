# Express + React Application

A full-stack web application built with **Express.js** for the backend API and **React** for the frontend interface.

## Tech stack

- **Frontend:** React.js
- **Backend:** Express.js / Node.js
- **Package manager:** npm

## Project structure

```text
.
├── client/       # React application
├── server/       # Express API
└── README.md
```

## Prerequisites

- Node.js 18 or newer
- npm

## Getting started

1. Clone the repository and enter the project directory.

   ```bash
   git clone <repository-url>
   cd <project-folder>
   ```

2. Install and start the Express server.

   ```bash
   cd server
   npm install
   npm run dev
   ```

3. In another terminal, install and start the React application.

   ```bash
   cd client
   npm install
   npm run dev
   ```

The React application is typically available at `http://localhost:5173`, while the Express API runs on the port configured by the server (commonly `http://localhost:5000`).

## Environment variables

Create a `.env` file in the `server` directory for server-side configuration. For example:

```env
PORT=5000
```

Do not commit files containing secrets. Add `.env` files to `.gitignore`.

## Available scripts

Common scripts include:

| Location | Command | Purpose |
| --- | --- | --- |
| `client` | `npm run dev` | Starts the React development server |
| `client` | `npm run build` | Creates a production frontend build |
| `server` | `npm run dev` | Starts the Express server in development mode |
| `server` | `npm start` | Starts the Express server in production mode |

Refer to each application's `package.json` for the exact scripts available.

## License

Add a license for this project if one is required.
