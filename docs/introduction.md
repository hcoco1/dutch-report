# 1. Introduction

## 1.1 Background

The Netherlands has a dense and interconnected transport environment involving railways, cycling, roads, and public transport.

Railway stations operate within this wider geographic environment. Their surrounding populations and transport infrastructure can differ considerably.

GIS provides a way to measure and compare these spatial differences.

## 1.2 Research question

> Which Dutch railway stations have the strongest multimodal environment for the population they serve?

## 1.3 Objectives

- Build a reproducible geospatial dataset of Dutch railway stations.
- Measure population and transport infrastructure around each station.
- Compare stations across the Netherlands.
- Identify spatial patterns.
- Communicate the results through maps and a GIS report.

## 1.4 Scope

- **Study area:** Netherlands
- **Unit of analysis:** Railway station
- **Catchment:** 1 km circular buffer

**Included:**

- Population
- Cycling infrastructure
- Major roads
- Public-transport stops
- Waterways as geographic context

**Excluded from Phase 1:**

- Routing
- Travel-time analysis
- Network analysis
- Passenger flows
- PostGIS
- FastAPI
- Leaflet
- React
