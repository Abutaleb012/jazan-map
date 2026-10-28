# Jazan City Maps: Points of Interest and Record Rainfall

Interactive maps of Jazan, Saudi Arabia, from the first days of my **300 Days Mapping Challenge**.

By **Ali Abutaleb, PhD** · [Portfolio](https://abutaleb012.github.io/)

## 1. Points of interest

**Live map:** [jazan_map.html](https://abutaleb012.github.io/jazan-map/jazan_map.html)

Where Jazan eats, meets, and studies: **710+ restaurants, 383 cafes, and 174 schools**, each clickable for its name, rating, and address.

**How it was built** (see `jazan_mapping_clean.ipynb`):

1. A grid of search points covers the city, because the Google Maps Places API returns at most 60 results per search.
2. Each category is searched in **both Arabic and English**, plus targeted street-level searches for places the grid misses.
3. Results outside the city are filtered out, and the city boundary comes from OpenStreetMap.
4. The final map uses a dark basemap, color-coded layers, popups, and a restaurant heatmap.

One finding: OpenStreetMap data for Saudi cities is far less complete than for Western cities, so combining sources and searching in both languages is essential.

Versions:

| File | Version |
|---|---|
| `jazan_map.html` | Desktop, English |
| `jazan_map_mobile.html` | Mobile, English |
| `jazan_map_arabic_mobile1.html` | Mobile, Arabic (latest) |
| `jazan_map_arabic_mobile.html` | Mobile, Arabic (earlier layout) |

## 2. Record rainfall, 2022

**Live card:** [jazan_2022_rainfall.html](https://abutaleb012.github.io/jazan-map/jazan_2022_rainfall.html)

CHIRPS daily rainfall from 1981 to 2025, analyzed in Google Earth Engine. In 2022 the Jazan region received nearly **370 mm**, the highest in 44 years of records, with more than 650 mm on the highlands and escarpment. Every year from 2023 to 2025 stayed above 300 mm, which suggests a shifted baseline rather than a one-off event.

`jazan_2022_rainfall_card (1).html` is an identical copy of the rainfall card.

## Built with

Python (GeoPandas, OSMnx, Folium), Google Maps Places API, OpenStreetMap, Google Earth Engine, and CHIRPS.

## Running the notebook

Open `jazan_mapping_clean.ipynb`, replace `YOUR_API_KEY_HERE` with your own Google Maps API key (Places API enabled), and run it top to bottom.
