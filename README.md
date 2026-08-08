# KONTUR 🌍

A geography quiz web app: recognize countries by their outline.
After each guess, distance (km/mi) and compass direction tell you where to look next.

**▶ Play:** https://llm-1998.github.io/KONTUR/

## Features

* **Solo mode** – 6 tries per country, region and difficulty selection (Easy to Expert, 26–233 countries), deck system with no repeats and a try-distribution chart at the end of each run
* **Daily challenge** – the same country for everyone worldwide, shareable emoji result, fully serverless (derived from a hash of the date)
* **Multiplayer** – real-time rooms for up to 4 players on their own devices: create a room, share a code or invite link, guess the same countries secretly and simultaneously, score by proximity (direct hit = 5,000 points), live lobby settings and an animated podium with collectible one-liners
* **Training mode** – multiple choice where the wrong answers are the geographically nearest neighbors, light spaced repetition and persistent mastery tracking
* **World globe** – an interactive 3D globe with real country borders (microstates included): search any country and fly there in a three-act camera move, double-tap to identify what you see, with a country panel showing flag, capital, population, continent and ISO code
* **Country index** – all 233 countries with large outline, flag, capital and population, each linked to the globe ("show me where this is")
* **Installable app (PWA)** – add it to your home screen for a fullscreen app with its own icon, playable offline
* Progressive hints (population → capital → flag), dark mode, German/English (incl. language-aware share links), km/miles

## Tech

A single HTML file at its core – no frameworks, no build step. Country outlines from
Natural Earth (hybrid 1:50m/1:10m) plus OSM data for microstates, simplified
with Douglas-Peucker; distances via the haversine formula between country centroids.
The globe renders the real Earth via orthographic projection (d3-geo, loaded on demand);
multiplayer runs on Firebase Realtime Database, loaded only when you play together.
Offline play is handled by a service worker (network-first with cache fallback).

