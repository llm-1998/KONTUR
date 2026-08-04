# KONTUR 🌍

A geography quiz web app: recognize countries by their outline.
After each guess, distance (km/mi) and compass direction tell you where to look next.

**▶ Play:** https://llm-1998.github.io/KONTUR/

## Features
- **Solo mode** – 6 tries per country, region and difficulty selection (Easy to Expert, 26–233 countries), deck system with no repeats and a try-distribution chart at the end of each run
- **Daily challenge** – the same country for everyone worldwide, shareable emoji result, fully serverless (derived from a hash of the date)
- **Training mode** – multiple choice where the wrong answers are the geographically nearest neighbors, light spaced repetition and persistent mastery tracking
- **Country index** – all 233 countries with large outline, flag, capital and population
- Progressive hints (population → capital → flag), dark mode, German/English, km/miles

## Tech
A single HTML file – no frameworks, no backend. Country outlines from
Natural Earth (hybrid 1:50m/1:10m) plus OSM data for microstates, simplified
with Douglas-Peucker; distances via the haversine formula between country centroids.

*Built in dialogue with Claude*
