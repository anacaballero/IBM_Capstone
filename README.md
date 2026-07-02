# Urban Neighborhood Intelligence — Geospatial Segmentation

Geospatial analysis system for profiling and clustering urban neighborhoods based on their venue mix, combining web scraping, REST API integration, and unsupervised learning.

## Problem

Neighborhood character is hard to quantify from census data alone. Venue density and category mix — what amenities exist, how concentrated they are — captures the texture of daily life and enables data-driven applications in urban planning, real estate, and relocation support.

## Approach

### Data Collection
- Neighborhood boundaries and postal codes scraped from Wikipedia using BeautifulSoup
- Geographic coordinates resolved via geocoding API
- Venue data retrieved from Foursquare API: category and frequency of venues within 500m of each neighborhood centroid

### Feature Engineering
Each neighborhood represented as a vector of venue category proportions across 50+ Foursquare categories, creating a comparable profile regardless of total venue count.

### Segmentation
K-means clustering groups neighborhoods by amenity similarity. Cluster profiles reveal distinct archetypes: entertainment-dense corridors, residential zones, transit-oriented districts.

### Visualization
Interactive Folium map with cluster overlays for spatial exploration of the segmentation results.

## Stack

`Python` `BeautifulSoup` `requests` `Foursquare API` `pandas` `scikit-learn` `folium` `geopy`
