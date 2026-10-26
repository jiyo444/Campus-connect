# CampusConnect — Student Marketplace (MERN)

React + Vite frontend, Express API, MongoDB Atlas database, JWT authentication, and CRUD listings.

## MongoDB setup
1. In MongoDB Atlas, create a free cluster and a database user.
2. In Network Access, allow your IP address. For temporary testing only, Atlas supports `0.0.0.0/0`; remove this later.
3. Choose Connect → Drivers → Node.js and copy the URI.
4. Copy `server/.env.example` to `server/.env`; replace the URI placeholders and set a long random JWT_SECRET. Never share `.env`.

## Run in Codespaces
Open two terminals from the repository root.
Terminal 1:
```bash
cd server && npm install && cp .env.example .env && npm run dev
```
Edit `server/.env` with your Atlas URI before using accounts/listings.
Terminal 2:
```bash
cd client && npm install && npm run dev
```
Open forwarded port 5173. The API uses port 5000.

Demo cards remain visible if the API/database is unavailable. Accounts and new listings require MongoDB to be connected. Photos are emoji placeholders in this starter; image upload is not included.
