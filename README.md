# awesome-berlin-transit [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome) [![RSS](https://img.shields.io/badge/Subscribe-RSS-blue.svg)](https://github.com/tifa365/awesome-berlin-transit/commits/main.atom)

##### Comprehensive collection of open-source tools, APIs, and datasets for Berlin public transport (VBB/BVG).

This list catalogs the extensive work by [@derhuerst](https://github.com/derhuerst) and others on Berlin's public transportation data ecosystem. From REST APIs to real-time monitoring, GTFS datasets to transit map generators.

------------------------------

### Table of Contents

- [APIs & Clients](#apis--clients)
- [Static Datasets & Helpers](#static-datasets--helpers)
- [Finding Stations](#finding-stations)
- [Extra Data About Berlin Transport](#extra-data-about-berlin-transport)
- [Realtime, Monitoring & GTFS-Realtime](#realtime-monitoring--gtfs-realtime)
- [Tools, UIs & Experiments](#tools-uis--experiments)
- [Mapping & Transit Map Generation](#mapping--transit-map-generation)
- [Text Parsing & Utilities](#text-parsing--utilities)
- [Gists & Configuration Files](#gists--configuration-files)

------------------------------

## APIs & Clients

REST APIs and JavaScript clients for accessing BVG/VBB/HAFAS data.

- [bvg-rest](https://github.com/derhuerst/bvg-rest) - Public REST API that wraps BVG's HAFAS data.
- [vbb-rest](https://github.com/derhuerst/vbb-rest) - REST API for the full VBB network.
- [vbb-hafas](https://github.com/derhuerst/vbb-hafas) - JS client for the VBB HAFAS backend.
- [hafas-client](https://github.com/derhuerst/hafas-client) - General HAFAS mobile API client used by VBB/BVG tools.
- [hafas-rest-api](https://github.com/derhuerst/hafas-rest-api) - Expose any HAFAS client via a REST API.
- [cached-hafas-client](https://github.com/derhuerst/cached-hafas-client) - Add caching to a HAFAS client.
- [hafas-client-rpc](https://github.com/derhuerst/hafas-client-rpc) - JSON-RPC bridge (WebSockets/stdio) for hafas-client.
- [observe-hafas-client](https://github.com/derhuerst/observe-hafas-client) - Observe departures/arrivals returned by hafas-client.

------------------------------

## Static Datasets & Helpers

Comprehensive datasets derived from VBB GTFS and other sources.

- [vbb-gtfs.jannisr.de](https://github.com/derhuerst/vbb-gtfs.jannisr.de) - Archive/mirror of VBB GTFS (historical + latest).
- [vbb-stations](https://github.com/derhuerst/vbb-stations) - Comprehensive station list (BVG & S-Bahn).
- [vbb-lines](https://github.com/derhuerst/vbb-lines) - Lines and their station sequences.
- [vbb-lines-at](https://github.com/derhuerst/vbb-lines-at) - Which lines call at a given station.
- [vbb-shapes](https://github.com/derhuerst/vbb-shapes) - Line geometries/shapes.
- [vbb-trips](https://github.com/derhuerst/vbb-trips) - "When do which trains stop where?" (derived from GTFS).
- [vbb-stations-connected-to](https://github.com/derhuerst/vbb-stations-connected-to) - Adjacency/connected stations graph.
- [vbb-translate-ids](https://github.com/derhuerst/vbb-translate-ids) - Convert 9-digit↔12-digit VBB IDs.
- [vbb-runs-every](https://github.com/derhuerst/vbb-runs-every) - Compute headways ("runs every 5m"). **Deprecated**
- [vbb-static](https://github.com/derhuerst/vbb-static) - Older monolith of GTFS-derived datasets. **Deprecated**

------------------------------

## Finding Stations

Search, autocomplete, and CLI tools for station discovery.

- [vbb-stations-autocomplete](https://github.com/derhuerst/vbb-stations-autocomplete) - Build autocomplete for station names.
- [vbb-find-stations](https://github.com/derhuerst/vbb-find-stations) - Station search helpers.
- [vbb-stations-cli](https://github.com/derhuerst/vbb-stations-cli) - Find & filter stations from the command line.

------------------------------

## Extra Data About Berlin Transport

Additional information and metadata about VBB/BVG infrastructure.

- [vbb-fare-zones](https://github.com/derhuerst/vbb-fare-zones) - AB/BC/ABC mapping for all VBB stations.
- [vbb-station-operators](https://github.com/derhuerst/vbb-station-operators) - Operator per station (BVG, S-Bahn etc.).
- [vbb-osm-relations](https://github.com/derhuerst/vbb-osm-relations) - OSM relation IDs for VBB lines/platforms/entrances.
- [siemensbahn-berlin](https://github.com/tifa365/siemensbahn-berlin) - OSM data extractor for the Siemensbahn railway line (relation 7382983) with exports to GeoJSON, Shapefile, and interactive HTML map.
- [vbb-station-photos](https://github.com/derhuerst/vbb-station-photos) - Photos for every Berlin U-Bahn station.
- [vbb-platform-patterns](https://github.com/derhuerst/vbb-platform-patterns) - U-Bahn platform tile color patterns.
- [vbb-stations-with-wifi](https://github.com/derhuerst/vbb-stations-with-wifi) - Free Wi-Fi spots/BSSIDs at stations.
- [vbb-stations-with-bicycle-parking](https://github.com/derhuerst/vbb-stations-with-bicycle-parking) - Bike parking near stations (from OSM).
- [vbb-logos](https://github.com/derhuerst/vbb-logos) - SVG logo set for VBB/BVG.
- [vbb-entrances](https://github.com/derhuerst/vbb-entrances) - Station entrance locations. **Outdated**
- [vbb-delays-list](https://github.com/derhuerst/vbb-delays-list) - Station delay statistics. **Unfinished**
- [vbb-graph](https://github.com/derhuerst/vbb-graph) - JSON Graph of the whole VBB network.
- [vbb-common-places](https://github.com/derhuerst/vbb-common-places) - Aliases for iconic places ("zoo", "alex", "kotti"…).
- [Der BER im 3D-Modell](https://interaktiv.tagesspiegel.de/lab/flughafen-ber-in-3d/) - Interactive 3D model explaining Berlin Brandenburg Airport's 14-year construction delays and technical problems.

------------------------------

## Realtime, Monitoring & GTFS-Realtime

Live data feeds, disruption tracking, and monitoring tools.

- [vbb-disruptions](https://github.com/derhuerst/vbb-disruptions) - Scrapes BVG & S-Bahn Berlin service disruptions.
- [sbahn-berlin-tweets](https://github.com/derhuerst/sbahn-berlin-tweets) - Parse @SBahnBerlin status tweets.
- [augment-vbb-hafas](https://github.com/derhuerst/augment-vbb-hafas) - Enrich VBB HAFAS responses with realtime from other sources.
- [vbb-positions-stream](https://github.com/derhuerst/vbb-positions-stream) - Live bus/train positions stream.
- [hafas-monitor-trips](https://github.com/derhuerst/hafas-monitor-trips) - Watch all trips in a bbox.
- [hafas-monitor-departures](https://github.com/derhuerst/hafas-monitor-departures) - Bulk monitor departures for many stations.
- [hafas-live-ws-server](https://github.com/derhuerst/hafas-live-ws-server) - WebSocket server broadcasting live HAFAS data.
- [hafas-monitor-trips-server](https://github.com/derhuerst/hafas-monitor-trips-server) - Server managing/serving monitors.
- [hafas-gtfs-rt-feed](https://github.com/derhuerst/hafas-gtfs-rt-feed) - Generate GTFS-Realtime by monitoring a HAFAS endpoint.
- [record-hafas-data](https://github.com/derhuerst/record-hafas-data) - CLI to record monitored data to LevelDB.
- [hafas-discover-stations](https://github.com/derhuerst/hafas-discover-stations) - Discover network topology via departures.
- [hafas-estimate-station-weight](https://github.com/derhuerst/hafas-estimate-station-weight) - Estimate station "importance".
- [hafas-monitor-journeys](https://github.com/derhuerst/hafas-monitor-journeys) - Monitor specific A→B journeys.
- [hafas-fetch-track-slice](https://github.com/derhuerst/hafas-fetch-track-slice) - Extract a leg's track slice between stops.
- [hafas-find-trips](https://github.com/derhuerst/hafas-find-trips) - Guess the vehicle you're in from location/bearing.
- [hafas-find-alternative-legs](https://github.com/derhuerst/hafas-find-alternative-legs) - Get alternatives for journey legs.
- [fetch-commute-from-hafas](https://github.com/derhuerst/fetch-commute-from-hafas) - Batch-fetch your commute journeys.

------------------------------

## Tools, UIs & Experiments

Interactive tools, bots, and experimental applications for Berlin transit.

- [vbb-cli](https://github.com/derhuerst/vbb-cli) - CLI for searching VBB journeys.
- [vbb-telegram](https://github.com/derhuerst/vbb-telegram) - Telegram bot for VBB.
- [vbb-map-routing](https://github.com/derhuerst/vbb-map-routing) - Map-based trip planning in Berlin.
- [vbb-journey-ui](https://github.com/derhuerst/vbb-journey-ui) - Journey component (Google-Maps-style).
- [vbb-delays-map](https://github.com/derhuerst/vbb-delays-map) - Interactive map of delays. **Outdated**
- [generate-vbb-gtfs](https://github.com/derhuerst/generate-vbb-gtfs) - Produce "clean" GTFS from VBB data.
- [vbb-stations-html](https://github.com/derhuerst/vbb-stations-html) - HTML index of all stations.
- [vbb-web](https://github.com/derhuerst/vbb-web) - Web client for VBB routing.
- [vbb-anybar](https://github.com/derhuerst/vbb-anybar) - Menu-bar reminder for when to leave for the train.
- [vbb-get-off-bot](https://github.com/derhuerst/vbb-get-off-bot) - Telegram bot that pings you before your stop.
- [monitor-hafas-cli](https://github.com/derhuerst/monitor-hafas-cli) - Terminal monitor for any HAFAS endpoint.
- [hafas-linked-connections-server](https://github.com/derhuerst/hafas-linked-connections-server) - Linked Connections endpoint from HAFAS.
- [berlin-commute-footprint](https://github.com/derhuerst/berlin-commute-footprint) - Cost/CO₂/health comparison: car vs PT vs bike. **Unfinished**
- [predict-vbb-delays](https://github.com/derhuerst/predict-vbb-delays) - Delay prediction experiments. **Unfinished**
- [vbb-routing](https://github.com/derhuerst/vbb-routing) - Route planner on VBB GTFS. **Unfinished**
- [naive-gtfs-routing](https://github.com/derhuerst/naive-gtfs-routing) - Simple GTFS routing engine. **Unfinished**
- [remix-bvg-map-frontend](https://github.com/derhuerst/remix-bvg-map-frontend) - Remix the BVG map (front-end).
- [remix-bvg-map-backend](https://github.com/derhuerst/remix-bvg-map-backend) - Backend for the map remixer.
- [bvg-topological-map](https://github.com/derhuerst/bvg-topological-map) - Official BVG network as a tagged SVG dataset.
- [BrokenLifts.org](https://brokenlifts.org/) - Real-time tracking of elevator and escalator outages across Berlin's public transport network. Shows which stations have accessibility issues, helping mobility-impaired passengers plan routes and avoid stations with broken lifts.
- [Berlin zählt Mobilität](https://lab.technologiestiftung.de/projects/berlin-zahlt-mobilitat/) - Open data platform for counting pedestrians and cyclists at measurement points across Berlin. Visualizes mobility patterns and traffic volumes to support evidence-based urban planning and the Verkehrswende (mobility transition).
- [Umweltzone Berlin](https://umweltzone.berlin/) - Interactive map showing Berlin's low-emission zone boundaries and regulations. Helps drivers understand where environmental badges are required and what restrictions apply to different vehicle types.
- [Infravelo Fahrradstraßen](https://www.infravelo.de/karte/) - Interactive map of Berlin's bike streets (Fahrradstraßen) where cyclists have priority and special rights. Shows current bike street infrastructure and planned projects. Bike streets play a central role in Berlin's secondary street network, increasing safety and making cycling more attractive.
- [Parken im Straßenraum](https://gdi.berlin.de/geonetwork/srv/api/records/3c507d6f-77d6-48bd-aa9b-0d6b3ed1d894) - Comprehensive dataset of all street parking spaces in Berlin. Complete coverage within the S-Bahn ring (95% accuracy as of July 2023) and outer areas (80% accuracy as of 2021). Available via WMS/WFS services. Data collected through street surveys, OpenStreetMap, and CityScanner technology. Published by Senate Department for Mobility, Transport, Climate Protection and Environment under DL-DE-Zero-2.0 license.
- [Critical Tracks](https://criticaltracks.k-nut.eu) - Interactive map visualizing Critical Mass bike rides in Berlin (and other cities when zoomed out). Position data is recorded during rides via the Critical Maps app, collected at intervals, and filtered the next day to protect privacy (only points with sufficient "neighbors" within ~100m remain visible). Visualization shows time-based playback of rides using mapbox-gl. Monthly JSON exports publicly available at [/data/](https://criticaltracks.k-nut.eu/data). By [@k-nut](https://github.com/k-nut). [Blog post](https://blog.k-nut.eu/critical-tracks).

------------------------------

## Mapping & Transit Map Generation

Tools for generating and rendering Berlin transit maps.

- [generate-vbb-graph](https://github.com/derhuerst/generate-vbb-graph) - Build a JSON Graph Format network.
- [generate-vbb-transit-map](https://github.com/derhuerst/generate-vbb-transit-map) - Auto-generate SVG transit map of Berlin.
- [OSM Berlin & Verkehrswende](https://github.com/osmberlin) - Organization hosting OpenStreetMap projects for sustainable transport and Berlin/Brandenburg. Includes parking data processing, traffic sign tools, street space maps, and Mapillary street coverage analysis. Active community with monthly meetups.
- [Straßenraumkarte Neukölln](https://strassenraumkarte.osm-berlin.org/) - High-resolution OSM basemap showing Neukölln's street space at architectural-plan detail: exact curb lines, bike lanes, parking spaces, trees, benches, bollards. Built from OSM micromapping + ALKIS data. Includes [Parkraumkarte](https://parkraum.osm-verkehrswende.de/) showing 30,000+ individual parking spots. [GitHub](https://github.com/osmberlin/strassenraumkarte-neukoelln), [OSM Wiki](https://wiki.openstreetmap.org/wiki/Stra%C3%9Fenraumkarte_Neuk%C3%B6lln).
- [transit-map-generator](https://github.com/derhuerst/transit-map-generator) - Interactive generator/optimizer. **Unfinished**
- [vbb-graph-computation-server](https://github.com/derhuerst/vbb-graph-computation-server) - Queue VBB map computations. **Unfinished**
- [vbb-map](https://github.com/derhuerst/vbb-map) - Render lines on a map. **Unmaintained**
- [vbb-osm-map](https://github.com/derhuerst/vbb-osm-map) - Render lines using OSM. **Unmaintained**
- [vbb-toy-map-feed](https://github.com/derhuerst/vbb-toy-map-feed) - Live feed for the delays map. **Unmaintained**
- [vbb-station-graph](https://github.com/derhuerst/vbb-station-graph) - Visualize network near a station. **Unmaintained**

------------------------------

## Text Parsing & Utilities

Utilities for parsing and normalizing VBB/BVG-specific text and data.

- [parse-vbb-station-name](https://github.com/derhuerst/parse-vbb-station-name) - Parse/normalize VBB/BVG station names (formerly vbb-tokenize-station).
- [vbb-short-station-name](https://github.com/derhuerst/vbb-short-station-name) - Strip noise like "(Berlin)", shorten "Straße→Str.".
- [vbb-line-colors](https://github.com/derhuerst/vbb-line-colors) - Canonical colors for VBB lines.
- [vbb-parse-line](https://github.com/derhuerst/vbb-parse-line) - Parse line IDs like M4, TXL, S42.
- [vbb-mode-weights](https://github.com/derhuerst/vbb-mode-weights) - Heuristic weights per mode in Berlin.
- [merge-vbb-stations](https://github.com/derhuerst/merge-vbb-stations) - Heuristic to merge stops that should be one. **Archived**
- [merged-vbb-stations](https://github.com/derhuerst/merged-vbb-stations) - Precomputed list from the merge heuristic.
- [vbb-parse-ticket](https://github.com/derhuerst/vbb-parse-ticket) - Parse HAFAS ticket info.
- [are-vbb-hafas-stations-the-same](https://github.com/derhuerst/are-vbb-hafas-stations-the-same) - Decide if two HAFAS stations are the same real place.
- [vbb-line-variant-score](https://github.com/derhuerst/vbb-line-variant-score) - Identify canonical line variants.

------------------------------

## Gists & Configuration Files

Useful gists and extracted configuration files.

- [VBB Android app config files](https://gist.github.com/derhuerst/a8d94a433358abc015ff77df4481070c) - Extracted HAFAS properties from the official app.
- [BVG Berlkönig HAFAS requests](https://gist.github.com/derhuerst/6fe0663338e542d7d35998990c623a69) - Sample HTTP calls for the Berlkönig integration.
- [List of HAFAS API Endpoints](https://gist.github.com/derhuerst/2b7ed83bfa5f115125a5) - Broad list of endpoints, useful for cross-checking BVG/VBB.

------------------------------

## Credits

This collection is primarily the work of [@derhuerst](https://github.com/derhuerst), who has created an incredible ecosystem of open-source tools for Berlin public transport data.

## License

[![CC0](http://i.creativecommons.org/p/zero/1.0/88x31.png)](http://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, the contributors to this list have waived all copyright and related or neighboring rights to this work.

Last updated: 2025-10-21
