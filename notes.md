# FOSS4G
Friday, 20th November, 2020.

## Antartica - Dave Bowden

He studies the distribution of seafloor biological communities and processes using cameras. 

### Quantarctica 

- A comprehensive collection of Antarctic geographical datasets for research, eduction, and environmental management.
- Compile dna formatted to work seamlessly with the free open-source software QGIS.
- A huge range of datasets are available.
- Facilitates spatial analysis of Antarctic data by providing a comprehensive set of up-to-date environmental layers in a single package.

## Using QGIS for open ocen ecosystems - Pablo Escobar

### Introduction 

- Study mid-trophic level organisms in open ocean ecoststems using active acoustics.
- Monitor distrbution and abundance.
- Develop predictive models for acoustic energy.
- Describe and charaterise acoustic aggregations.
- Relate species or groups to environmental variables.

### QGIS 

Use Quantartica to create figures for research.

### Quantarctica

[Download](https://www.npolar.no/quantarctica/)

Quantarctica is a collection of Antarctic geographical datasets for research, education, operations, and management in Antarctica.

### Questions 

Q1. Quantarctica has a default projection for that region.
A1. We can rotate the map in QQIS, or invert the presentation of the projection.

## NiSOS - Andrea Mari 

- NIWA deployed underwater towed/drop cameras to record seabed videos.
- Staff view the videos (both in real time and after donwloading it)

### Process 

- Vessel arrives at survey site.
- Multibeam survery to map seabed. 
- DEM created, transect location decided.
- Multi screen workspace.

### Workflow 

1. Create or open a database to record observations/messages.
2. Create or open a layout (the screen with the items which can be recorded)
3. Create a session (who is recording, when, what)
4. Create or open a station.
5. For a recorded video - open the video file, or just view the live video picture.
6. Start observation recording.
7. End recording/session.

### Software 

- NiSOS was devloped as a Java application.
- Spqatialite library for SQLite, they use the latest version.
- It is a state application, steps must be completed in order (similar to Weka).
- We store the location and time in the database on sqlite. Stored as a pointm.
- This approach reduces the number of records, providing a huge performance boost.
- Listens to geographic data transmitted by the ship with UDP.
- SQLITE is a file, threading had to be managed, to prevent concurret writing to the database.

## Visual Perception and Cartigrahpy - Pete King 

- Visual perception and Gestalt.
- Our retinas do not perceive that much information.
- Gestalt = "pattern" or "configuration".
- The quality of the whole is different to the sum of the parts.

### Gestalt

- Emergence - the tendency to perceive the whole before we consciosly examine its contents. 
- Invariance - the tendency to percieve a deisgnated whol as a constant in its characteristics.
- Multi-stability - the ability to see multiple while at the same time or quickly alternate between percieved wholes.
- Reification - the process of recongistion.

- Law of Paraganaz 
- Similarity 
- Proximity
- Continuity
- Closure
- Symmetry
- Connectedness 

### Figure ground
- elements are percieved as either figures (Distinct elemnts of focus) or ground (the background).
- used in cartography te emphasize the relationship between layers and figures.
- convex, complicated, symmety and verticality.

### Conclusion 
- if we understand how we you can be  more purposeful in our choices.
- don't use all techniques at once.
- add to or remove.

## NZGB - LINZ 

- New Zealand Geographical Board - NZGB 
- [website](https://www.linz.govt.nz/regulatory/place-names/about-new-zealand-geographic-board)
- Record of place names for New Zealand.
- BLM, want to change place names, no proposals so far.

### What is a name? 

- Official place names have been certified by the board.
- Purpose: practical unambigious location identification && recognise cultural heritage.

### Gazatteer 

```
gazetteer
/ˌɡazəˈtɪə/
Learn to pronounce
noun
noun: gazetteer; plural noun: gazetteers
a geographical index or dictionary
```

- the countries authoratative list of place names.
- [Gazetteer](https://gazetteer.linz.govt.nz/)
- keeps records of decisions made by the board.
- New Zealand Geographic Board Act 2008.
- Gazatteer information must be provided to the public.
- 6 separate spreadsheets were made available on the LINZ website.
- A postgreSQL database.
- spatial editing via QGIS plugin.
- added custom url for each unique placename id.
-[search](https://gazetteer.linz.govt.nz/place/23582)

### Stack 
1. postgres/postgis database.
2. QGIS (via custom plugin for mist data management activities, clisely coupled to the dataase structure). 
3. Leaflet.
4. LINZ data service hoosted by Koordinates, using Open Street Maps.

## DGGS - Byron Cochraine

- catologues, linked data and geo-sptaital data. 
- Dicrete Global Grid Systems - DGGS.
- a fractal approach to spatial data and analysis. 
- globally unique cell indices.
- from analog to digital.
- Open Geospatial Consortium. 
- OGC Testbed 16.
- D3 Uber, for congestion pricing. 
- pigeon tool - python.
- covid tracing app using D3.
- starts with comparison for comparing locations.

## PyGeoAPI.io - Tim-Hinnerk Heuer
- OGC API 
- Convoluted: WFS, WMS, OWS
- Collectios 
- Better for web crawlers to index
- Tool to simplify existing map services

## LiDAR - Rose Philips 

```
Lidar, which stands for Light Detection and Ranging, is a remote sensing method that uses light in the form of a pulsed laser to measure ranges (variable distances) to the Earth.Aug 3, 2020

What is lidar? - NOAA's National Ocean Service
oceanservice.noaa.gov › facts › lidar
```

- at the frontier of vector and raster geospatial data.
- perks: ground penetration through vegetation.  
- large volume of data storage required. 
- archaeology papers show the potential for LiDAR data in discvovering new sites and exposing old sites.
- machine learning can be used for feature detection in LiDAR data. 
- vegetation rates are affected by dead bodies, US studies have shown.
- R lidR libary.
- "Identifying trees uring.

### Tools 

- LASTools 
- R libraries: lidR, raster, rdal
- CloudComapre

## Retrieving & Anlaysing 'cloud-native' satellite imagery with R - Anthony Pengelly

- free software environment that is great for data science.
- shiny makes building web apps (relatively) easy.
- interopreable with a lot of other tools: python, QGIS, etc...
- very quick and readible data analysis ability.
- "15cm" true colour imagery.
- SpatioTemporal Asset Catalogue (ATAC)
- Cloud Optimized GeoTIFF (COG)

```
SAR is a type of active data collection where a sensor produces its own energy and then records the amount of that energy reflected back after interacting with the Earth.

What is Synthetic Aperture Radar? | Earthdata
earthdata.nasa.gov › learn › what-is-sar
```

## Static Vector Tiles - Ian Reese 

- avoid complex server setups for web services.
- easy to set up for testing project in a web environment.
- only one data set we needed to work with.
- work in the NZTM on the web.
- option to test using localhost.

```
Web Mercator is a slight variant of the Mercator projection, one used primarily in Web-based mapping programs. It uses the same formulas as the standard Mercator as used for small-scale maps.

Web Mercator projection - Wikipedia
en.wikipedia.org › wiki › Web_Mercator_projection
```

```
New Zealand Transverse Mercator 2000 (NZTM2000) is the projection used for New Zealand's Topo50 1:50,000 and other small scale ...

New Zealand Transverse Mercator 2000 (NZTM2000) | Land ...
www.linz.govt.nz › data › geodetic-system › projections
```

### Tools 

- uncrompressed vector protobuf file (.pbf)
- SimpleHTTPServer 
- GitPages 
- `l.vectorGird.protobuf()` 
- this reads tile caches on the fly from the tile cache.

### Cons 

- PBFs are uncompressed 
- T-Rex still a bit buggs for custom projection.
- T-Rex: custom vectors and vector tiling.
- create rich tile vector caches in desired projections. 
- doesn't work well for maps with too many tiles.
- good for robustness, with large scale feature layers.
- for contours that are gigabytes in size, that need to be served on the web.

## Pacific Soil Portal - David Medychyj-Scott 

- big problems in the pacific related to soil.
- soil degredation, erosion, land pollution.

### Stack 

- soil maps are served via WMTS from geoserver's geowebcache.
- geoserver provides layer metadata via CSW.
- base maps are using Open Streem Map and ESRI's World _Image_Layer.
- predominant mobile use in the Pacific Islands, rather than traditional desktop.

### GeoSpatial Stack 

- QGIS, PostGIS, Geoserver, GeoNode, MapStore.
- open source vs vendor.
- make ArcGis great again.
- vendor locking can introduce large costs.
- feature development funding is driven by the community not a market.
- is vendor lock-in being driven by dumbing down of GIS skills and blinkering.
- is innovation rdecreasing as organisations accept vendors word as gospels.

## Keynote 

## Ethics - Tom MacWright

### Backstory

- Engineer at Mapbox.
- the problem is that most maps are tiled.
- each bit of geographical data was a seperate tiny image file.
- this took forever to transfer USB files.
- created MBTiles, by putting map information on a Spatialite database.
- that was sort of like MBTiles, but had some special features, like measuring cloud cover 
- eventually, it was clear, well: it was imaging drones.
- "All things truely wicked start from innocense" - Hemmingway

### Questions  

1. Does it matter who creates things? 
    - it was designed by flemmish sailor to navigate the earth

2. Does it matter why things are created? 
    - European Petroleum Survey Group: EPSG: 4326

3. Does the original purpose matter? 
    - The K in KML is for "keyhole".
    - the company was acquired by Google.
    - most commerical map technology is ad driven.

4. Does it matter how it's used?
    - how the U.S military buys location data from ordinary apps.

5. Are ethics universal?

### Opensource 

- copyright law - you have infinite wishes.
- open source - I wish for now wished, for me or anyone.

### Ethos licensing 

- A controverisal alternative form of open source licesning that takes ethical position.
- the JSON license, the Hippocratic License, and others are different variations.
- In essence, an open source license that tries to restrict people from using you software for ill.

"This Software shall be used for Good, not Evil." 
- Brent's [IBM](https://en.wikipedia.org/wiki/Douglas_Crockford) analogy.

### Artist - Grayson Cook 

- data scientists often use fmap to remove cloud coverage.
- this creates large troves of cloud coverage data.
- explore enourmous variance in cloud data across a transect of Australia.
- clouds are vital, they reflect solar rays, and facilitate the rain cycle.
- 270 GB of 7 years of cloud data across path 99.
- cloud colour plummets across the country in 2019.
- Australia's hottest year, also preface to their wildfires.
- Animate cloud data and project onto a land mass. 
- This becomes a show at the NZ Carter Observatory.

## Open source - Nathan Woodrow

- open source is just code.
- open source is people.
- between the code is the people.
- find poeple you enjoy talk with.
- open source contributions provides good mentorship.
- look outside you community for inspiration on being better.
- check the ego. Don't act like a rock star.
- be the person you wish your community to be.
- people have livs oustide of open source.
- having other hobbies is such a crazy idea it works.
- open source connections can be great career opportunities.

## Open data - Litea Biukoto 

- risk informed decisions and investments. 
- Fiji - Cyclone Winston in numbers. 
- 540,000 affected, 60,000 people displaced, 44 deaths.
- issues countered when accessing hazard risk related information.
- require agreed standards.
- coherence across different systems/processes. 
- an inhouse software developer is essential.
- not all data is create equal.
- access and availablity to re-use data. 
- [PacRIS](http://pcrafi.spc.int/)

## ABC Canbera - Markis Mannheim

- data journalist _not_ a data scientist.
- engaging users in communicating geospatial data.
- we stare at maps quite often, electorial college map.
- most of the time media use maps, they are used as abstract charts of data.
- if you keep things simple, the user will understand the message. 
- the three second rule for user engagement.
- data visualizations that can be understood pre-cognitively.
- anything beyond three colours, and the user starts having to think.
- maps are one of the only form of graph that lends itself towards 3D.

## Geospatial network analysis with R - Shrividya Ravi

- networks quantify relaionships between entities 
- example: intersections become nodes, streets are edges 
- sfnetworks 

## Linz Data Service Plugin 

- A plugin in for QGIS. 
- stream publihed datasets from the LINZ data servevice.
- quick way to add basemap and feature layers.

## TimescaleDB - Brent

- NIWA maintains a database of sensor readings from instruments installed on its research vessle Tangaroa.
- postigs, timescaledb, hstore.
- postgis - continues to evolve, adding functionality for spatial data managment.
- timescaledb - does for timeseries data what Postgis does for spatial data (automated paritioning of tables, functions)
- hstore - implements key/value pairs and operatos/function to interact with them (no need for JSONB in this use case)
- No. records: 1.2b -> 13.6m.
- relative space required: 1 -> 0.1.
- typical performance: 1 -> 3-40x faster.
- functionality: identical but much simpler data.