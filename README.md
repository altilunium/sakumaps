# saku.maps
Manage your saved coordinates locally

https://user-images.githubusercontent.com/70379302/186137469-16d3ec98-22c5-46e5-b63a-65b0174ac5c1.mp4




## Problem
I want to save coordinates data, whether it's places that i've visited or someone's address. Back then, i'm using Google Maps, or QGIS to store this data, but i'm quite unsatisfied. 

## How To Use

### Add New Coordinate by Using Map
1. Click the blue button
2. Click the coordinate on the map
3. Click the green button to continue adding new data, click the red button to cancel
4. Add coordinate's note. Type something
5. Click the green button to save

### Add New Coordinate by using (Lat,Lon) data
Export data from Google Map and store locally in sakumaps

![image](https://user-images.githubusercontent.com/70379302/186134095-547d3cce-ed7c-452f-a576-b7b488405e5f.png)
1. Open Google Maps, find your place, right click, click the coordinate data. Your (lat,lon) data will be copied to clipboard
2. Open Pocketmap, press `Ctrl+.` , paste your (lat,lon) data.
3. Click the blue button and proceed as usual

### Manage The Database
![image](https://user-images.githubusercontent.com/70379302/186135322-c70b7f31-4f44-4b11-b7d2-f732d5ad47be.png)
1. Open sakumaps by using Chromium-based browser. Right click anywhere, click developer tools.
2. Click "application" tab, click "indexedDB" pane.
3. You can delete your data here.

### Hide The Basemap
![](src.png)
Sometimes you just want to see the spatial distribution of your collected coordinates data, without distractions. Press `Ctrl+,` to hide the basemap. Press it once more to show it back.

### Advanced Custom Styling
Different color for different type of coordinates? Sure. Just modify the `async function ref()` source code. 

## Tech Stacks
1. [Leaflet.js](https://leafletjs.com) : Basemap renderer, add new point
2. [Dexie.js](https://dexie.org) : IndexedDB Wrapper
