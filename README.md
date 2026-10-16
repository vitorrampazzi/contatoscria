# Contact Manager

A Next.js and React learning project for listing, filtering, and managing contacts. It explores controlled forms, React hooks, API requests, and browser caching.

## Features

- Load contacts from a MockAPI endpoint.
- Filter contacts by name, email, or phone number.
- Add and remove contacts in local application state.
- Display contact statistics.
- Cache contact data in `localStorage` with a five-minute expiry.
- Show loading, error, and connection states.
- View individual contacts through a dynamic route.

Contact additions and removals in the main page update local state and the browser cache; they are not persisted to the remote API. A later successful API response can replace those local changes.

## Technology

- Next.js
- React
- JavaScript
- Tailwind CSS
- Axios

## Project structure

```text
app/
├── components/
├── contact/[id]/
├── utils/
│   ├── api.js
│   └── cache.js
├── layout.js
└── page.js
```

## Run locally

Install Node.js and npm, then run:

```bash
git clone https://github.com/vitorrampazzi/contatoscria.git
cd contatoscria
npm install
npm run dev
```

Open [localhost:3000](http://localhost:3000).

The Axios configuration is in `app/utils/api.js`. The current implementation reads the `/contacts` resource from a MockAPI service.

## Available commands

| Command | Purpose |
| --- | --- |
| `npm run dev` | Start the development server |
| `npm run build` | Build the application |
| `npm start` | Start the production server after building |
| `npm run lint` | Run ESLint |
