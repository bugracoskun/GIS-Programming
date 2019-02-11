# GIS-Programming
This repository contains the data, information and code about the content of the "GMT 456 GIS Programming" course offered at the Geomatics Engineering Dept. of Hacettepe University, Turkey.

The developed code is based on Python as it allows to further extend into a QGIS plugin.

## Contents:
* Object oriented programming - A Recap
   * Function Calls – pass by reference vs pass by value
   * Signal- Slot
* Graph Data Structure
   * Adjacency Matrix
   * Disjoint Sets
   * Minimum Spanning Tree
      * Kruskal's Algorithm
      * Prim's Algorithm
* Building a QGIS Plugin

## Methodology
1. Import the polygon shapefile into PostGIS
2. Create the *centroids* table
     1. gid (geometry_id) - serial
     2. name - varchar(40)
     3. geom (geometry) - geometry(point,*SRID*)
3. Populate the centroids table (st_centroid)
4. Create the *edges* table
    1. gid (geometry_id) - serial
    2. origin - text
    3. destination - text
    4. cost (weight) - float
    5. geom (geometry) - geometry(LineString, *SRID*)
    6. origin_gid - integer
    7. destination_gid - integer
5. Populate the edges table (at_intersects) 

* An exemplary SQL code is included under the *SQL* directory

     
