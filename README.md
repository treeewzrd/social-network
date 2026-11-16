# Social Network API

![Status](https://img.shields.io/badge/status-coursework-blue)

Coursework REST API for users, thoughts, reactions, and friend relationships.

**Built with:** TypeScript, Node.js, Express, MongoDB, Mongoose.

## Run locally

Requires Node.js/npm and MongoDB. From the repository root:

```bash
npm ci
cp .env.example .env
```

Skip the copy if `.env` already exists. Configure `MONGODB_URI` privately, then run:

```bash
npm start
```

Start compiles TypeScript and launches the API. Use an API client to exercise the routes under `/api/users` and `/api/thoughts`.

## Scope

This is a data-modeling and routing exercise, not a production social network. Use sample records. `npm test` is a placeholder; the declared seed command references a file not present in the current source.

Setup instructions were checked against source; builds and application behavior have not been rerun during this cleanup.
