# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

- **Start server**: `npm start` (runs `node app.js` on port 3000)
- **Development**: `npm run devv` (uses nodemon for auto-restart — note the script has a typo: `nodemon app js` instead of `nodemon app.js`, fix if nodemon isn't restarting properly)
- No test suite is configured.

## Architecture

**This project is actively being scaled and will grow significantly.** The README outlines an ambitious roadmap including a team builder, battle simulator, PWA support, advanced filtering, and a full backend with user accounts and a database. Keep this growth trajectory in mind when making architectural decisions — prefer patterns that scale and avoid dead-end designs.

This is currently a minimal Express.js static file server with a vanilla JS frontend. The backend does no data processing — it only serves files and handles routing.

### Backend (`app.js`)

Three routes map to three separate HTML pages:

| Route | Serves |
|-------|--------|
| `GET /` | `index.html` (home) |
| `GET /about` | `About/about.html` |
| `GET /pokemon` | `Pokemon/pokemon.html` |

Each route also mounts its directory as a static file server so relative asset paths (CSS, JS) resolve correctly.

### Frontend

All Pokémon data (386 entries covering Kanto, Johto, Hoenn) is hardcoded in `Pokemon/pokedex.js` as a plain JS array. There is no database or backend API.

**Data flow in `Pokemon/pokedex.js`:**
1. A filtered copy of the Pokémon array is passed to `render(list)`
2. `render()` creates DOM card elements dynamically
3. Images are fetched from the PokeAPI GitHub sprites repo (`raw.githubusercontent.com/PokeAPI/sprites/master`) — animated GIFs first, with fallback to static PNGs via `onerror`
4. Clicking a card calls `openModal(pokemon)` to show a details overlay

**Each Pokémon entry shape:**
```js
{ id, name, types: [], entry: "Pokédex description" }
```

**Event-driven filtering:** The search input and shiny toggle both call `render()` with the current filtered list on every change.
