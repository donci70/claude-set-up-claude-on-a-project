# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

A small Express.js REST API with an in-memory data store (no real database).

## Commands

- `npm run dev` — start with auto-restart on http://localhost:3000
- `npm test` — run all tests (`node --test tests/users.test.js` for a single file)
- `npm run lint` — run ESLint

## Architecture

- `server.js` exports `app` without calling `.listen()` when required, so tests drive it directly with supertest instead of a real port.
- `routes/` — one router file per resource, mounted in `server.js`.
- `db/store.js` — in-memory store; not persisted, resets on restart.

## Conventions

- Routes never touch data directly — reads/writes go through `db/store.js`.
- New resources get their own router file in `routes/`, mounted in `server.js`, following `routes/users.js`.
- use hungarian notation on variable names
