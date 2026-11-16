# Social Network API

![Status](https://img.shields.io/badge/status-coursework-blue)

Coursework REST API for users, thoughts, reactions, and friend relationships.

**Built with:** TypeScript, Node.js, Express, MongoDB, Mongoose.

## What I built

- Implemented Express routes and controllers for users, thoughts, reactions, and friendships.
- Designed Mongoose schemas with relationships, validation, and calculated fields.
- Added create, read, update, and delete operations for the API's records.

## Explore the source

- [src/controllers/user-controller.ts](src/controllers/user-controller.ts) — User and friendship operations.
- [src/controllers/thought-controller.ts](src/controllers/thought-controller.ts) — Thought and reaction operations.
- [src/models/User.ts](src/models/User.ts) — User schema and relationships.

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
