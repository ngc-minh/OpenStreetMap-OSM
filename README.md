# 🗺️ Urban Map Prototype with OpenStreetMap

Prototype web maps for Hanoi built on **OpenStreetMap** and **Leaflet**: flood-risk zones, live location, temperature markers, and a small alert API.

![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Leaflet](https://img.shields.io/badge/Leaflet-199900?style=flat-square&logo=leaflet&logoColor=white)
![OpenStreetMap](https://img.shields.io/badge/OpenStreetMap-7EBC6F?style=flat-square&logo=openstreetmap&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-404040?style=flat-square&logo=express&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)

## Pages

| File | What it shows |
|---|---|
| `index2.html` | **Flood map**: GeoJSON polygons of local flooding areas in four risk levels (rarely, occasionally, often, frequently flooded), each with a popup |
| `osm.html` | **Live location**: the user's current position from the browser Geolocation API |
| `osm01.html` | **Temperature markers** with popups |
| `check.html` | Animated marker experiment |

## Alert API

`server.js` is an Express + MongoDB backend for map alerts:

| Method | Endpoint | Body / result |
|---|---|---|
| `POST` | `/api/alerts` | `{ type, latitude, longitude, message }` |
| `GET` | `/api/alerts` | List of all alerts |

## Run it

The map pages are static. Open them directly in a browser, or serve the folder:

```bash
npx serve .
```

To run the API, set your MongoDB connection string in `server.js` (`mongoURI`), then:

```bash
npm install
node server.js        # http://localhost:3000
```

## Status

Student prototype. The original goal was an application for managing urban energy and resources from OpenStreetMap data; the full proposal (in Vietnamese) is in [`docs/proposal-vi.md`](docs/proposal-vi.md).
