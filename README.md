Digpro Bright
==========

![screenshot](https://raw.github.com/digpro-group/dp-bright/master/preview.png)

Digpro Bright is meant to be a general background map.

It is based on OSM Bright (https://github.com/mapbox/osm-bright)

Setup Instructions
------------------

### 1. Download shapefiles

Digpro Bright depends on three shapefiles. You will need to download and extract them before continuing. 

Download them to the `shp` directory in the dp-bright folder. You can do this with `wget` like:

    mkdir dp-bright/shp
    cd dp-bright/shp
    wget https://osmdata.openstreetmap.de/download/simplified-land-polygons-complete-3857.zip
    wget https://osmdata.openstreetmap.de/download/land-polygons-split-3857.zip
    wget http://mapbox-geodata.s3.amazonaws.com/natural-earth-1.4.0/cultural/10m-populated-places-simple.zip

Once downloaded, extract them from their zip files.

    unzip simplified-land-polygons-complete-3857.zip
    unzip land-polygons-split-3857.zip 
    unzip 10m-populated-places-simple.zip

### 2. Run the shapefiles through shapeindex

    shapeindex *.shp */*.shp

### 3. Convert style sheet to XML

    carto dp-bright.mml > dp-bright.xml

