# Quiet Water Finder

Finds public land beside ponds, streams, springs and wetlands anywhere in the US, ranked by how unvisited each spot looks. Made for finding places to photograph aquatic insects: dragonflies, damselflies, mayflies, stoneflies, caddisflies and water bugs.

Open it: https://briangooding.github.io/quiet-water-finder/

## How it works

Everything runs in the browser, one `index.html` with no build step. Each search pulls live data from:

- **Public land:** USGS Protected Areas Database (PAD-US), with its public-access codes
- **Water:** USGS National Hydrography Dataset (1:24k streams, ponds, marshes, springs, waterfalls)
- **Parking and trailheads:** OpenStreetMap via Overpass (optional; the public servers are often busy)
- **Insect records and visitor counts:** iNaturalist
- **Place search:** Photon (OpenStreetMap data)

Each stretch of water that touches public land becomes a spot. The **hidden score** goes up for unnamed water, springs and small ponds, distance from parking, and few iNaturalist records nearby. It goes down for big lakes, spots right by parking, and restricted access.

PAD-US access codes are a guide, not a permit. Check the land manager's rules before you go.

## Running locally

Open `index.html` in a browser, or serve the folder with `python -m http.server`.
