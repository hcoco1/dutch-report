# 4. Methodology

## 4.1 Coordinate reference system

All spatial calculations will use:

**EPSG:28992 — Amersfoort / RD New**

## 4.2 Station catchment

A **1 km circular buffer** will be created around each railway station.

The same catchment will initially be used for all primary metrics.

## 4.3 Population

The project will use the CBS 100 m population grid.

Population will be aggregated using the **centroid-in-buffer** method. A population grid cell contributes to a station when its centroid falls inside the station's 1 km catchment.

**Limitation:** a cell can partially overlap the catchment while its centroid falls outside it.

## 4.4 Cycling infrastructure

Measure the total length of qualifying cycling infrastructure within 1 km of each station.

Metric: `cycling_km_1km`

The exact OpenStreetMap tagging rules will be documented during data preparation.

## 4.5 Roads

Measure the total length of `primary`, `secondary`, and `tertiary` roads within 1 km of each station.

Metric: `road_km_1km`

## 4.6 Public transport

Count public-transport stops within 1 km of each railway station.

Metric: `pt_stops_1km`

## 4.7 Station-level dataset

The final analytical dataset will contain, at minimum:

- `station_id`
- `station_name`
- `population_1km`
- `cycling_km_1km`
- `road_km_1km`
- `pt_stops_1km`
- `geometry`

## 4.8 Classification

**To be determined after inspecting the data distributions.** The classification method will not be selected until the metrics have been calculated and examined.

## 4.9 Validation

The analysis will check:

- duplicate stations
- missing geometries
- invalid geometries
- CRS consistency
- unmatched spatial joins
- missing values
- invalid or suppressed population values
