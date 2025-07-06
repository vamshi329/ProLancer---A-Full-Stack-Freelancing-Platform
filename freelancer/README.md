# Freelancer Application

This repository contains a full-stack freelancer marketplace MVP split into two packages:

| Folder | Tech | Purpose |
| ------ | ---- | ------- |
| `client-*/client` | React (Create React App) | Front-end single-page application |
| `server-*/server` | Node + Express, MongoDB (Mongoose), Socket.IO | REST / WebSocket back-end |

> The *timestamp* folders (e.g. `client-20250616T052048Z-1-001`) were created by the export process—inside them you will find the actual `client` and `server` projects.

---

## Prerequisites
* Node.js ≥ 18 (both client & server)
* npm (comes with Node)
* MongoDB running locally or a connection string for a remote cluster (if you intend to persist data)

---

## Quick Start

### 1. Install dependencies
```bash
# CLIENT (Terminal 1)
cd client-*/client
npm install

# SERVER (Terminal 2)
cd server-*/server
npm install
```

### 2. Run in development mode
Open **two** terminals and execute the following:

```bash
# Terminal 1 – Front-end (http://localhost:3000)
cd client-*/client
npm start

# Terminal 2 – Back-end (http://localhost:5000)
cd server-*/server
npm start
```

*The exact back-end port can be adjusted inside `server/index.js`. The React dev server will proxy API/WebSocket calls if you add a `proxy` field in `client/package.json`.*

---

## Building for production
```bash
cd client-*/client
npm run build  # outputs static files to build/
```
Host the contents of `build/` on any static hosting service (Netlify, Vercel, S3, etc.).

For the server, deploy the `server` folder to a Node-capable platform such as Render, Railway, or Fly.io.

---

## Environment Variables
No environment variables are required out-of-the-box. When you integrate a real database or auth system, create a `.env` file inside the `server` folder and load it with [dotenv](https://www.npmjs.com/package/dotenv).

---

## Linting & Testing
* CRA is pre-configured with ESLint, Jest, and React Testing Library.
* Back-end tests are not yet set up—add your preferred framework (Jest, Mocha, etc.).

---

## Useful Scripts
| Location | Command | Description |
| -------- | ------- | ----------- |
| `client` | `npm start` | Runs React dev server with hot reload |
|          | `npm run build` | Produces an optimized production bundle |
| `server` | `npm start` | Starts Express/Socket.IO server (ES modules) |

---

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

---

## License
MIT
