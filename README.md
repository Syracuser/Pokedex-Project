# Pokédex Web App

![Pokémon Logo](https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/other/official-artwork/25.png)

A feature-rich Pokédex built with PokéAPI that lists Pokémon, supports search by name, types, abilities, and evolutions, with pagination/infinite scroll — fully responsive on mobile and desktop.

---

## About This Project

This is a full-stack Pokédex application that allows users to browse, search, and view detailed information about Pokémon. It fetches live data from the [PokéAPI](https://pokeapi.co/), a free and open Pokémon RESTful API.

The app is served via a lightweight **Node.js + Express** backend that handles routing and static file serving, with a clean multi-page frontend built in plain HTML, CSS, and JavaScript.

One small detail I'm particularly proud of: each Pokémon card displays its real Pokédex ID number, keeping it faithful to the actual Pokédex numbering.

---

## Current Features

- Browse all Pokémon with pagination / infinite scroll
- Search Pokémon by name
- View detailed info: stats, types, abilities, and evolutions
- Individual Pokémon detail pages
- About page
- Fully responsive — works on mobile and desktop
- 404 fallback for invalid routes

---

## Tech Stack

- **Backend:** Node.js, Express 5
- **Frontend:** HTML, CSS, JavaScript
- **API:** [PokéAPI](https://pokeapi.co/)

---

## Installation & Running

```bash
git clone https://github.com/your-username/pokedex.git
cd pokedex
npm install
npm start
```

Then open your browser to **http://localhost:3000**

For development with auto-restart:
```bash
npx nodemon app.js
```

---

## Planned Improvements

### ⭐ Advanced Filtering System

Filter Pokémon by:
- Type (Fire, Water, Dragon, etc.)
- Generation
- Height / weight
- Base stat ranges
- Legendary / Mythical

### 👥 Pokémon Team Builder

Build a team of 6 Pokémon with:
- Add / remove Pokémon
- Team stat totals
- Type weakness analysis
- Type coverage overview
- Save team to localStorage

### ⚡ Smart Caching

Cache Pokémon data in `localStorage` to:
- Reduce API calls
- Speed up load times
- Demonstrate performance optimization

### 🔍 Live Search Suggestions

Show autocomplete suggestions while typing (e.g. typing `pi` shows Pikachu, Pidgey, Pinsir).

### 📊 Pokémon Comparison Tool

Compare two Pokémon side-by-side with a stat table and bar charts.

### 🎨 Type-Based Theming

Dynamically change the UI color theme based on the selected Pokémon's type (e.g. Fire → red, Water → blue, Ghost → purple).

### 🧬 Evolution Tree Visualization

Display evolution chains as a visual tree, including branching evolutions like Eevee's.

### 📥 Offline Mode (PWA)

Convert the app into a Progressive Web App:
- Installable on devices
- Works offline
- Uses service workers and caching strategies

### ⭐ Small But Powerful Features

- **Favorites** — save a list of favourite Pokémon
- **Dark Mode** — toggle dark/light theme
- **Pokémon Cry Sound** — play the Pokémon's cry audio
- **Random Pokémon Button** — discover a random Pokémon

### 🧠 Battle Simulator Lite

A lightweight battle calculator:
- Input two Pokémon
- Calculate type effectiveness
- Estimate damage output

---

## Future Backend Expansion

Planned backend features using Node.js, Express, and MongoDB/PostgreSQL:

- User accounts
- Save favourite Pokémon
- Save and share teams
- Persist search history

---

## Screenshots

_Coming soon_

---

## License

[MIT](LICENSE)
