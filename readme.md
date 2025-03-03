# My First Web Map - The Diamondback 

## Introduction
For this webmap information on the route for the diamondback was used. Multiple stops that could be useful aswell as some of the names for sections of the route were mapped out aswell. A brief description and aswell as a summary of the route were made to help the user understand what they are looking at aswell as a hyperlink to the main page of the diamondback. 

## Major Functions
- <a href="https://diamondback226.com/" target="_blank">Diamondback</a> : Used to hyperlink the main diamond back page to the summary portion of the map
-  style : function(feature): Used to edit the style of the route
- var route = L.geoJson(data, {filter : function(feature) {if(feature.geometry.type =="LineString") {return feature}}}) : Used to insert the route itself
- var myStops = L.geoJson(data, {filter : function(feature){if(feature.geometry.type =="Point") {return feature}}}): Used top insert stops along the route  
- onEachFeature : function(feature, layer) {layer.bindTooltip(feature.properties['name'])} : Used to mkae the stops interactive showing the name of the stops when hovering over them

## Libraries Used
- [Leaflet](https://leafletjs.com/) - Used for the base map   

## Data Sources
- [Google Maps](https://www.google.com/maps) - Used for map data and location services  
- [GeoJSON.io](https://geojson.io/) - Source for geographic data formatting  
- [The Diamondback](https://dbknews.com/) - Used for relevant news or location-based information